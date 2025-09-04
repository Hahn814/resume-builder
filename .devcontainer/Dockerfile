FROM python:3-bookworm


WORKDIR /usr/src/builder
COPY requirements.txt ./ 
RUN pip install --no-cache-dir -r requirements.txt \
    && apt-get update \
    && apt-get install -y pandoc texlive-xetex texlive-fonts-recommended texlive-plain-generic \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
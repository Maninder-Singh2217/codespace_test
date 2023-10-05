# Use the official Codespaces image as a base
FROM mcr.microsoft.com/codespaces/ubuntu:dev

# Install necessary packages
RUN sudo apt-get update && \
    sudo apt-get install -y cmake make g++ && \
    sudo apt-get clean

# Install Google Benchmark library (replace with the appropriate installation method)
RUN git clone https://github.com/google/benchmark.git && \
    cd benchmark && \
    cmake -E make_directory build && \
    cmake -E chdir build cmake -DCMAKE_BUILD_TYPE=Release .. && \
    cmake --build build --target install

# Set the working directory
WORKDIR /workspace

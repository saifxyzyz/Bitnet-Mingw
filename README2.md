Used mingw instead of visual studio

cmake -B build -S . -G "MinGW MakeFiles" -DCMAKE_CXX_STANDARD=11 -DCMAKE_CXX_COMPILER=C:/msys64/bin/g++.exe -DCMAKE_CXX_FLAGS="-D_WIN32_WINNT=0x0602" -DGGML_NATIVE

cmake --build build --config Release

python run_inference.py -m models/BitNet-b1.58-2B-4T/ggml-model-i2_s.gguf -p "Hi how are you doing, who are you?\nAnswer:" -n 6 -temp 0

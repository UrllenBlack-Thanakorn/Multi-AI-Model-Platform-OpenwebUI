#Requirement for setup

python3 -m venv .aider-env
source .aider-venv/bin/activate

#forcoding model run this

llama-server -m ~/models/qwen2.5-coder-7b-q4_k_m.gguf \
  --port 50055 \
  -c 16384 \
  -ngl 99 \
  --alias qwen2.5-coder-7b

#for chat run this

llama-server -m ~/models/Qwen2.5-7B-Instruct-Q4_K_M.gguf \
  --port 50056 \
  -c 16384 \
  -ngl 99 \
  --alias qwen2.5-7b-chat

for image scaner run this

#llama-server -m ~/models/qwen2-vl-7b-q4_k_m.gguf \
  --mmproj ~/models/mmproj-qwen2-vl-7b-f16.gguf \
  --port 50057 \
  -c 8192 \
  -ngl 99 \
  --alias qwen2-vl-7b

#llama-server \
  -m ~/models/gpt-oss-20b-Q3_K_M.gguf \
  --port 5005ค \
  -c 16384 \
  -ngl 99 \
  --alias gpt-oss-20b

#Intergrate all with chat ui like chat gpt , gemini, cluaude, etc. run openweb ui

 .aider-env/bin/open-webui serve --host 127.0.0.1 --port 3000

 On openwebui add your local link to connect ai yo openwebui system

# AgentDyn<center>

# AgentDyn: A Dynamic Open-Ended Benchmark for Evaluating Prompt Injection Attacks  of  Real-World Agent Security System

AgentDyn is a dyanmic open-ended agent security benchmark built on top of the AgentDojo framework.

## Quickstart

```bash
pip install -e .
```


## Running the benchmark

For adaptability, we support an evaluation script similar to AgentDojo's. Documentation on how to use the script can be obtained with the `--help` flag.

For example, to run the `shopping` suite , with `gpt-4o-2024-08-06` as the LLM, the tool filter as a defense, and the attack with important_instructions, run the following command:

```bash
python -m agentdojo.scripts.benchmark -s shopping \
    --model GPT_4O_2024_08_06 \
    --defense tool_filter --attack important_instructions
```

Before running, please export your API key, through:

1. OpenAI Model: export OPENAI_API_KEY=XXX
2. Google Model: export GOOGLE_API_KEY=XXX
3. Open-sourced Models (Qwen, LlaMA): export OPENROUTER_API_KEY=XXX

**Avaliable Suites:** AgentDyn supports `shopping`,`github`, and `dailylife` suites.

**Avaliable Models:** We evaluate the following models in our paper: ``GPT_4O_MINI_2024_07_18``, ``GPT_4O_2024_08_06``, ``GEMINI_2_5_FLASH``, ``GEMINI_2_5_PRO``, ``LLAMA_3_3_70B``, ``QWEN3_235B``, ``GPT_5_1_2025_11_13``, ``GPT_5_MINI_2025_08_07``.



## Inspect Results

To review the results reported in our paper, please refer to the log files in the ``(runs/)``.
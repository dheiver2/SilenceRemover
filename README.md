
# SilenceRemover

SilenceRemover é uma ferramenta para remover automaticamente trechos silenciosos de vídeos, utilizando Python, MoviePy e Pydub. Essa ferramenta é ideal para editar vídeos de forma a destacar partes relevantes, eliminando silêncios indesejados.

## Recursos

- Detecta e remove partes silenciosas de um vídeo.
- Utiliza o MoviePy para manipulação de vídeo e o Pydub para análise de áudio.
- Suporta a extração de áudio de vídeos.

## Requisitos

Certifique-se de ter as seguintes bibliotecas instaladas:

- `moviepy`
- `pydub`
- `ffmpeg` (requerido para processamento de áudio e vídeo)

Você pode instalar as dependências necessárias com o seguinte comando:

```bash
pip install -r requirements.txt
```

O arquivo `requirements.txt` deve conter:

```
moviepy==1.0.3
pydub==0.25.1
```

## Uso

Para usar o SilenceRemover, você pode executar o script Python diretamente. Certifique-se de substituir `"video.mp4"` pelo caminho do seu vídeo e `"output.mp4"` pelo nome do arquivo de saída desejado.

```python
from SilenceRemover import SilenceRemover

# Exemplo de uso
if __name__ == "__main__":
    remover = SilenceRemover("video.mp4", "output.mp4")
    remover.remove_silence()
```

## Como Funciona

1. **Carrega o vídeo**: O script carrega o vídeo a partir do caminho especificado.
2. **Extrai o áudio**: O áudio é extraído e salvo temporariamente.
3. **Detecta silêncios**: O Pydub é utilizado para detectar intervalos de silêncio no áudio.
4. **Corta e concatena**: O vídeo é cortado nos intervalos não silenciosos e os clipes são concatenados.
5. **Salva o resultado**: O vídeo final é salvo com o nome especificado.

## Contribuição

Se você deseja contribuir para este projeto, fique à vontade para fazer um fork e enviar pull requests.

## Licença

Este projeto está licenciado sob a MIT License - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

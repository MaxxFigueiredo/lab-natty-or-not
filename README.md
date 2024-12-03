# Título do Projeto Acessibilidade Inteligente para PCD 🤖♿

## 📒 Descrição
Este projeto tem como objetivo desenvolver um sistema baseado em Inteligência Artificial (IA) para melhorar a acessibilidade e autonomia de pessoas com deficiência (PCD). A solução proposta foca na criação de um assistente virtual inclusivo, capaz de interpretar comandos de voz, linguagem de sinais e fornecer suporte em tempo real para atividades cotidianas.

## 🤖 Tecnologias Utilizadas
Python: Linguagem para o desenvolvimento do sistema central.
Reconhecimento de Voz (Speech Recognition): Para interpretar comandos verbais.
Visão Computacional (OpenCV): Para reconhecimento de linguagem de sinais.
IA Generativa (ChatGPT): Respostas contextualizadas e suporte em tempo real.
Raspberry Pi: Para a criação de um dispositivo portátil e acessível.

## 🧐 Processo de Criação
Planejamento e Pesquisa: Identificação das necessidades específicas da comunidade PCD, como tradução de comandos de voz para texto ou leitura de linguagem de sinais.
Desenvolvimento do Assistente: Implementação do reconhecimento de voz e sinais com feedback em áudio ou texto.
Teste de Usabilidade: Avaliação com usuários PCD para garantir que o sistema seja intuitivo e funcional.
Documentação: Registro detalhado do desenvolvimento, com tutoriais para implementação e uso.
Exemplo de Código:
python
Copiar código
import speech_recognition as sr
import pyttsx3

def reconhecimento_voz():
    reconhecedor = sr.Recognizer()
    motor_fala = pyttsx3.init()

    with sr.Microphone() as source:
        print("Diga algo...")
        audio = reconhecedor.listen(source)

    try:
        comando = reconhecedor.recognize_google(audio, language="pt-BR")
        print(f"Você disse: {comando}")
        motor_fala.say(f"Você disse: {comando}")
        motor_fala.runAndWait()
    except sr.UnknownValueError:
        motor_fala.say("Desculpe, não entendi.")
        motor_fala.runAndWait()

reconhecimento_voz()

## 🚀 Resultados
Protótipo funcional que reconhece comandos de voz em português.
Sistema adaptado para tradução de comandos simples em linguagem de sinais.
Feedback em áudio para usuários com deficiência visual.

## 💭 Reflexão (Opcional)
Criar uma ferramenta de acessibilidade reforça a importância da tecnologia inclusiva. Este projeto mostrou como a IA pode ser um grande aliado para promover independência e melhorar a qualidade de vida de PCD. O desafio foi tornar o sistema eficiente em ambientes com ruído, mas ajustes futuros podem melhorar a experiência.

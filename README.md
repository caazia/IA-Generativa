# Explorando os Recursos de IA Generativa com Copilot e OpenAI


#### Explore a IA generativa com o Microsoft Copilot 
Neste exercício você explorará a IA generativa com o Microsoft Copilot.

Faça login no Microsoft Copilot
Abra copilot.microsoft.com e entre com sua conta pessoal da Microsoft.

O Microsoft Copilot usa IA generativa para aprimorar os resultados de pesquisa do Bing. O que isto significa é que, diferentemente da pesquisa apenas, que retorna conteúdo existente, o Microsoft Copilot pode reunir novas respostas com base na modelagem de linguagem natural e nas informações da web.

Na parte inferior da tela, você verá uma janela Pergunte-me qualquer coisa . À medida que você insere prompts na janela, o Copilot usa todo o thread da conversa para retornar respostas. Por exemplo, vamos tentar fazer uma série de perguntas sobre viagens.

![alt text](image-1.png)

![alt text](image-2.png)



#### Use prompts para gerar respostas 

Digite um prompt: What are 3 pros and cons of traveling in the winter?. Você verá Searching for:… e Generating… aparecer antes da resposta. O modelo usa as respostas pesquisadas como informação de base para gerar respostas originais. Observe que o final da resposta contém links para suas fontes.

![alt text](image.png)

Nota : Se você não vir uma mensagem *Generating… ou uma resposta de lista com marcadores, você ainda não conseguiu ver o Copilot em ação. Você precisa retornar ao menu de login e conectar a conta atual que está usando com uma conta pessoal.

Digite um prompt: Find me 3 more pros. O que você quer dizer com esta mensagem é que gostaria de ver mais três motivos positivos para viajar no inverno que ainda não foram listados. Observe que, com esse prompt, você está solicitando ao Copilot que faça duas coisas que a pesquisa por si só não faz: usar a resposta do chat anterior para excluir o que é retornado na nova resposta e usar o tópico do chat anterior sem declará-lo explicitamente.

Digite um prompt: Where are 3 places I can go to find fewer crowds?.

Observação : observe que, embora o Copilot seja capaz de fornecer uma resposta relacionada, ele pode eliminar “memórias” anteriores do tópico da conversa à medida que continua. Como resultado, as respostas que você obtém podem não estar diretamente relacionadas às viagens no inverno. Isso tem muito a ver com limitações de entrada de token. Quando o chat “lembra” partes anteriores de uma conversa, é porque economizou uma certa quantidade de tokens da conversa. À medida que novos tokens são introduzidos por meio de suas novas solicitações e respostas, o chat irá liberar os tokens mais antigos.

O botão Novo tópico próximo à janela de bate-papo é útil. Clicar nele limpa o tópico da conversa anterior para que as respostas do novo tópico não sejam baseadas no tópico anterior. Use o ícone Novo tópico próximo à janela de bate-papo para limpar seu histórico de mensagens.

![alt text](image-3.png)


#### Experimente a geração de imagens 

Agora vamos ver um exemplo de geração de imagens. Digite um prompt: Create an image of an elephant eating a hamburger. Observe que uma mensagem que tentarei criar que… aparece antes que o Copilot retorne uma resposta.

![alt text](image-4.png)

É importante notar que a resposta pode parecer semelhante, mas não igual. Isso ocorre porque as respostas são variadas.

Na resposta, há um texto na parte inferior que diz “Powered by DALL-E”. Considere como o DALL-E é baseado em grandes modelos de linguagem, à medida que sua entrada de linguagem natural gera imagens.

Retorne ao chat do Copilot clicando no ícone do Microsoft Bing no canto superior direito da tela.



#### Experimente a geração de código 

Agora vamos ver um exemplo de geração e tradução de código. Digite um prompt: Use Python to create a list.

Digite no prompt: Translate that into C#. Observe como você não precisou especificar o que é “aquilo”, como o Copilot sabe para se referir ao histórico de conversas.

![alt text](image-5.png)

![alt text](image-7.png)

using System;
using System.Collections.Generic;

namespace MyNamespace
{
    class Program
    {
        static void Main(string[] args)
        {
            List<object> myList = new List<object>
            {
                10, 20, 30, "apple", "banana", true
            };

            foreach (var item in myList)
            {
                Console.WriteLine(item);
            }
        }
    }
}



#### Tarefa bônus 

Digite um prompt: What are 3 examples of generative AI helping people?. Você pode usar isso como uma forma de debater suas próprias ideias de copiloto!


![alt text](image-8.png)

Resposta do Copilot:

Copilot
Certainly! Generative AI has made significant strides in various fields, benefiting people in practical ways. Let’s explore three examples:

Healthcare Applications:
Conversational AI Apps for Patients: Take Ada, for instance. It’s a doctor-developed symptom assessment app that offers medical guidance in multiple languages. By combining human expertise with AI, Ada supports improved health outcomes and delivers exceptional clinical excellence1.
Early Disease Detection: The SkinVision app uses AI for early detection of skin cancer. Through regulated medical services and expert input, it educates users on self-examination, risk understanding, and immediate concerns1.
AI for Accessibility: The Virtual Volunteer (also known as Be My Eyes) app assists visually impaired individuals. Powered by GPT-4, it instantly converts images into text, providing real-time identification, interpretation, and conversational visual assistance1.
Patient Interactions and Support: Hyro, a conversational AI, is designed specifically for health systems. It enhances patient engagement, automates common interactions, and helps overcome staffing shortages1.
Drug Discovery and Research:
Generative AI trained on scientific data aids researchers. For example, medical researchers use it to develop new molecular structures, while physicists test how different elements interact2.
Content Creation and Creativity:
Generative AI is used for content automation, style transfer, simulations, music composition, and image super-resolution. Tools like Scribe, TensorFlow, PyTorch, OpenAI GPT-3, and NVlabs StyleGAN enable creative applications3.
These examples demonstrate how generative AI is leaving a profound imprint on various aspects of our lives, from healthcare to creativity. 🌟🤖




### Explore o Azure OpenAI 

O Azure OpenAI Service traz os modelos generativos de IA desenvolvidos pela OpenAI para a plataforma Azure, permitindo-lhe desenvolver soluções poderosas de IA que beneficiam da segurança, escalabilidade e integração de serviços fornecidos pela plataforma de nuvem Azure.

Neste exercício, você explorará o serviço Azure OpenAI e o usará para implantar e experimentar modelos de IA generativos.

Este exercício levará aproximadamente 25 minutos.


### Provisionar um recurso Azure OpenAI 

Antes de poder utilizar modelos Azure OpenAI, deve fornecer um recurso Azure OpenAI na sua subscrição do Azure.

Entre no portal do Azure .
Crie um recurso Azure OpenAI com as seguintes configurações:

Assinatura : uma assinatura do Azure que foi aprovada para acesso ao serviço Azure OpenAI.
Grupo de recursos : escolha um grupo de recursos existente ou crie um novo com um nome de sua preferência.
Região : Escolha qualquer região disponível.
Nome : Um nome exclusivo de sua escolha.
Nível de preços : Padrão S0
Aguarde a conclusão da implantação. Em seguida, acesse o recurso Azure OpenAI implantado no portal do Azure.

![alt text](image-9.png)

![alt text](image-10.png)

Não foi possível realizar o lab de Open AI.

### Conclusão

O Microsoft Copilot representa uma verdadeira revolução na forma como nos relacionamos com a tecnologia. Suas habilidades de gerar texto, imagens e código a partir da linguagem natural abrem novos horizontes tanto para programadores quanto para a comunicação em geral. Com sua inteligência artificial avançada, o Copilot não apenas simplifica a vida dos desenvolvedores, mas também democratiza o acesso à tecnologia. No entanto, como toda tecnologia emergente, é crucial lembrar que o Copilot é uma ferramenta de auxílio, não um substituto para o discernimento humano. À medida que continuamos a explorar suas possibilidades, devemos também considerar as implicações éticas e de privacidade associadas a essa jornada. O futuro é promissor, e o Microsoft Copilot representa um passo significativo nessa trajetória.

### Links

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/12-generative-ai.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/13-azure-openai.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/14-azure-openai-content-filters.html

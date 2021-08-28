---
title: Accesso al controllo nelle pagine Web
description: Accesso al controllo nelle pagine Web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb6476ebdf2d26f1aec12a2f46506b3c4882d06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882964"
---
# <a name="accessing-the-control-in-web-pages"></a>Accesso al controllo nelle pagine Web

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per accedere ai servizi di Microsoft Agent da una pagina Web, usare il tag OBJECT HTML &lt; &gt; all'interno di <HEAD> o &lt; elemento BODY della &gt; pagina, che specifica il CLSID Microsoft (identificatore di classe) per il controllo. Usare inoltre un parametro CODEBASE per specificare il percorso del file di installazione di Microsoft Agent e il relativo numero di versione.

Se Microsoft Internet Explorer (versione 3.02 o successiva) è installato nel sistema, ma Microsoft Agent non è ancora installato e l'utente accede a una pagina Web con il tag OBJECT con il CLSID dell'agente, il browser tenterà automaticamente di scaricare Agent dal sito &lt; &gt; Web Microsoft. All'utente verrà quindi chiesto se procedere con l'installazione. Per altri browser, contattare il fornitore per informazioni relative al supporto o al supporto di terze parti per ActiveX controllo.

L'esempio seguente illustra come usare il parametro CODEBASE per scaricare automaticamente la versione in lingua inglese 2.0 di Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Agent può anche essere installato dal server HTTP o come parte del processo di installazione di un'applicazione. Per supportare l'installazione dal proprio server HTTP, è necessario inviare il file CAB autoinstallato di Microsoft Agent .Exe e specificarne l'URL nel tag CODEBASE.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Per supportare il download automatico di un componente del linguaggio di Microsoft Agent da una pagina Web, includere il tag Object del componente della lingua nella pagina prima del tag Object del controllo di Agent:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

dove XXXX viene sostituito con un ID lingua. Per le lingue attualmente supportate, vedere il sito Web Microsoft Agent.

-   Il &lt; tag OBJECT per un componente del &gt; linguaggio deve precedere &lt; il tag OBJECT per il componente principale di Microsoft &gt; Agent.
-   È possibile installare più lingue nello stesso client.
-   Prima di impostare [**languageID**](https://www.bing.com/search?q=**LanguageID**) di un carattere, è consigliabile che lo script verifichi che le impostazioni locali del browser, disponibili nella proprietà [**userLanguage,**](https://www.bing.com/search?q=**userLanguage**) corrispondano alla lingua impostata.

Per supportare altre versioni del linguaggio di Agent, usare un altro tag Object che specifica il componente del linguaggio. Tenere tuttavia presente che il tentativo di installare più lingue contemporaneamente può richiedere il riavvio dell'utente. I componenti del linguaggio di Agent possono essere ottenuti dal sito Web di Agent usando la stessa procedura del componente principale di Agent. Le licenze di distribuzione per i componenti del linguaggio sono coperte dalla licenza di distribuzione standard di Agent. Per iniziare a usare un carattere, è necessario caricare il carattere usando il [**metodo Load.**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) Un carattere può essere caricato dalla memoria locale dell'utente o da un server HTTP. Per altre informazioni sulla sintassi per il caricamento di un carattere, vedere il **metodo Load.** Al termine del caricamento del carattere, è possibile usare i metodi, le proprietà e gli eventi esposti dal controllo Agent per programmare il carattere. È anche possibile usare i metodi, le proprietà e gli eventi esposti dal linguaggio di programmazione e dal browser per programmare il carattere. ad esempio per programmarne la reazione al clic di un pulsante. Consultare la documentazione del browser per determinare quali funzionalità espone nel modello di scripting. Per microsoft Internet Explorer, vedere scripting object model, disponibile in ActiveX SDK.

I servizi dell'agente rimangono caricati solo quando è presente almeno un'applicazione client con una connessione. Ciò significa che quando un utente si sposta tra pagine Web abilitate per Agent, Agent verrà arrestato e tutti i caratteri caricati scompariranno. Per mantenere Agent in esecuzione tra le pagine e quindi mantenere visibile un carattere, creare un altro client che rimane caricato tra le modifiche della pagina. Ad esempio, è possibile creare un set di frame HTML e dichiarare un &lt; tag OBJECT per Agent nel frame &gt; padre. È quindi possibile creare script per le pagine caricate nei frame figlio, per chiamare lo script dell'elemento padre. In alternativa, è anche possibile includere un &lt; tag OBJECT in ogni pagina &gt; caricata nel frame figlio. In questo caso, tenere presente che ogni pagina sarà il proprio client. Potrebbe essere necessario usare il [**metodo Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) per impostare quale client ha il controllo quando l'utente interagisce con la pagina padre o figlio.

 

 

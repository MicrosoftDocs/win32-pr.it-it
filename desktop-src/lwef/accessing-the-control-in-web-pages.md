---
title: Accesso al controllo nelle pagine Web
description: Accesso al controllo nelle pagine Web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a965d73f7277b2b4a62c08a949782488f1e4dba4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725191"
---
# <a name="accessing-the-control-in-web-pages"></a>Accesso al controllo nelle pagine Web

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per accedere ai servizi di Microsoft Agent da una pagina Web, usare il <OBJECT> tag HTML nel <HEAD> oppure <BODY> elemento della pagina, che specifica il CLSID Microsoft (identificatore di classe) per il controllo. Usare inoltre un parametro codebase per specificare il percorso del file di installazione dell'agente Microsoft e il relativo numero di versione.

Se nel sistema è installato Microsoft Internet Explorer (versione 3,02 o successiva), ma Microsoft Agent non è ancora installato e l'utente accede a una pagina <OBJECT> Web con il tag con l'agente CLSID, il browser tenterà automaticamente di scaricare l'agente dal sito Web Microsoft. A questo punto, all'utente verrà chiesto se procedere con l'installazione. Per gli altri browser, rivolgersi al fornitore per informazioni relative al supporto o al supporto di terze parti per i controlli ActiveX.

Nell'esempio seguente viene illustrato come utilizzare il parametro codebase per scaricare il download della versione in lingua inglese 2,0 di Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Agent può anche essere installato dal server HTTP o come parte del processo di installazione di un'applicazione. Per supportare l'installazione dal server HTTP, è necessario pubblicare il file CAB di installazione automatica di Microsoft Agent. File exe e specificare il relativo URL nel tag codebase.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Per supportare il download automatico di un componente della lingua di Microsoft Agent da una pagina Web, includere il tag oggetto del componente della lingua nella pagina prima del tag Object del controllo agente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

dove XXXX viene sostituito con un ID di lingua. Per le lingue attualmente supportate, controllare il sito Web Microsoft Agent.

-   Il <OBJECT> tag per un componente del linguaggio deve precedere il <OBJECT> tag per il componente principale di Microsoft Agent.
-   È possibile installare più lingue nello stesso client.
-   Prima di impostare il [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) di un carattere, è consigliabile che lo script verifichi che le impostazioni locali del browser, disponibili nella proprietà [**UserLanguage**](https://www.bing.com/search?q=**userLanguage**) , corrispondano alla lingua impostata.

Per supportare altre versioni in lingua di Agent, è possibile usare un altro tag Object che specifica il componente del linguaggio. Tuttavia, tenere presente che il tentativo di installare più lingue contemporaneamente potrebbe richiedere l'avvio del riavvio dell'utente. I componenti della lingua dell'agente possono essere ottenuti dal sito Web dell'agente utilizzando la stessa procedura usata per il componente core dell'agente. Le licenze per la distribuzione per i componenti del linguaggio sono incluse nella licenza standard per la distribuzione degli agenti. Per iniziare a usare un carattere, è necessario caricare il carattere usando il metodo [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) . Un carattere può essere caricato dalla risorsa di archiviazione locale dell'utente o da un server HTTP. Per ulteriori informazioni sulla sintassi per il caricamento di un carattere, vedere il metodo **Load** . Una volta completato il caricamento del carattere, è possibile usare i metodi, le proprietà e gli eventi esposti dal controllo Agent per programmare il carattere. È anche possibile usare i metodi, le proprietà e gli eventi esposti dal linguaggio di programmazione e dal browser per programmare il carattere; ad esempio, per programmare la reazione a un clic del pulsante. Consultare la documentazione del browser per determinare le funzionalità che espone nel modello di scripting. Per Microsoft Internet Explorer, vedere il modello a oggetti di scripting, disponibile in ActiveX SDK.

I servizi dell'agente rimangono caricati solo quando esiste almeno un'applicazione client con una connessione. Ciò significa che quando un utente si sposta tra pagine Web abilitate per l'agente, l'agente verrà arrestato e tutti i caratteri caricati scompariranno. Per mantenere l'agente in esecuzione tra le pagine (mantenendo quindi un carattere visibile), creare un altro client che rimanga caricato tra le modifiche della pagina. Ad esempio, è possibile creare un frame HTML e dichiarare un <OBJECT> tag per Agent nel frame padre. È quindi possibile generare uno script per le pagine caricate nei frame figlio, per chiamare lo script del padre. In alternativa, è anche possibile includere un <OBJECT> tag in ogni pagina caricata nel frame figlio. In questo caso, tenere presente che ogni pagina sarà il proprio client. Potrebbe essere necessario utilizzare il metodo [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) per impostare il client che dispone del controllo quando l'utente interagisce con la pagina padre o figlio.

 

 
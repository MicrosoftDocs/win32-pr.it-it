---
title: Aggiunta di funzionalità di Microsoft Agent all'applicazione
description: Aggiunta di funzionalità di Microsoft Agent all'applicazione
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf604a7e18d67865fb50981833ce808985e455118326c4f157258543e236dd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753130"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Aggiunta di funzionalità di Microsoft Agent all'applicazione

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per accedere alle interfacce server di Microsoft Agent, Agent deve essere già installato nel sistema di destinazione. L'installazione diversa dall'uso del file eseguibile autoinstallato di Agent, ad esempio il tentativo di copiare e registrare i file dei componenti di Agent, non è supportata. In questo modo si garantisce un'installazione coerente e completa. Si noti che il file auto-installazione di Microsoft Agent non verrà installato in Microsoft Windows 2000 e nei sistemi operativi successivi perché queste versioni del sistema operativo includono già la propria versione di Agent.

Per installare correttamente Agent in un sistema di destinazione con un sistema operativo Microsoft Windows precedente, è necessario assicurarsi anche che il sistema di destinazione abbia una versione recente del runtime di Microsoft Visual C++ (Msvcrt.dll), dello strumento di registrazione Microsoft (Regsvr32.dll) e delle DLL COM Microsoft. Il modo più semplice per assicurarsi che i componenti necessari siano nel sistema di destinazione è richiedere l'installazione di Microsoft Internet Explorer 3.02 o versione successiva. In alternativa, è possibile installare i primi due componenti disponibili come parte di Microsoft Visual C++. Le DLL COM necessarie possono essere installate come parte dell'aggiornamento di Microsoft DCOM, disponibile nel sito Web Microsoft. Altre informazioni e informazioni sulle licenze per questi componenti sono disponibili nel sito Web Microsoft.

I componenti del linguaggio di Agent possono essere installati nello stesso modo. Analogamente, è possibile usare questa tecnica per installare il formato ACS dei caratteri Microsoft disponibili per la distribuzione dal sito Web Microsoft Agent. I file di caratteri vengono installati automaticamente nella \\ sottodirectory Chars di Microsoft Agent.

Poiché i componenti di Microsoft Agent sono progettati come componenti del sistema operativo, Agent potrebbe non essere disinstallato. Analogamente, se Agent è già installato come parte del Windows operativo, è possibile che l'archivio auto-installazione di Agent non venga installato.

Dopo l'installazione, per chiamare le interfacce di Agent, creare un'istanza del server e richiedere un puntatore a un'interfaccia specifica che il server supporta utilizzando la convenzione COM standard. In particolare, la libreria COM fornisce una funzione API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), che crea un'istanza dell'oggetto e restituisce un puntatore all'interfaccia richiesta dell'oggetto. Richiedere un puntatore [**all'interfaccia IAgent**](iagent.md) o [**IAgentEx**](iagentex.md) nella **chiamata CoCreateInstance** o in una chiamata successiva a [**QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

Il codice seguente illustra questa operazione in C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Se il server Microsoft Agent è in esecuzione, questa funzione si connette al server. in caso contrario, avvia il server.

Si noti che le interfacce del server Microsoft Agent includono spesso interfacce estese che includono un suffisso "Ex". Queste interfacce derivano da e pertanto includono tutte le funzionalità delle relative controparti non Ex. Se si vuole usare una delle funzionalità estese, usare le interfacce Ex.

Le funzioni che accettano puntatori a BSTR allocano memoria [**usando SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). È responsabilità del chiamante liberare la memoria usando [**SysFreeString.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

 

 
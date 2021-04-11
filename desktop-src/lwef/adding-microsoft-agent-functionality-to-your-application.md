---
title: Aggiunta della funzionalità Microsoft Agent all'applicazione
description: Aggiunta della funzionalità Microsoft Agent all'applicazione
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337078"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Aggiunta della funzionalità Microsoft Agent all'applicazione

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per accedere alle interfacce del server dell'agente Microsoft, è necessario che Agent sia già installato nel sistema di destinazione. Non è supportata l'installazione, ad eccezione del file eseguibile di installazione automatica dell'agente, ad esempio il tentativo di copiare e registrare i file dei componenti dell'agente. In questo modo si garantisce un'installazione coerente e completa. Si noti che il file di installazione automatica di Microsoft Agent non viene installato nei sistemi operativi Microsoft Windows 2000 e versioni successive, perché queste versioni del sistema operativo includono già la propria versione di Agent.

Per installare correttamente Agent in un sistema di destinazione con un sistema operativo Microsoft Windows precedente, è necessario verificare anche che il sistema di destinazione disponga di una versione recente di Microsoft Visual C++ Runtime (Msvcrt.dll), Microsoft Registration Tool (Regsvr32.dll) e Microsoft COM DLLs. Il modo più semplice per garantire che i componenti necessari si trovino sul sistema di destinazione, è necessario che sia installato Microsoft Internet Explorer 3,02 o versione successiva. In alternativa, è possibile installare i primi due componenti disponibili come parte del Microsoft Visual C++. Le DLL COM necessarie possono essere installate come parte dell'aggiornamento Microsoft DCOM, disponibile nel sito Web Microsoft. Per ulteriori informazioni e informazioni sulle licenze per questi componenti, vedere il sito Web Microsoft.

I componenti della lingua dell'agente possono essere installati nello stesso modo. Analogamente, è possibile utilizzare questa tecnica per installare il formato ACS dei caratteri Microsoft disponibili per la distribuzione dal sito Web Microsoft Agent. I file di caratteri vengono installati automaticamente nella \\ sottodirectory chars di Microsoft Agent.

Poiché i componenti di Microsoft Agent sono progettati come componenti del sistema operativo, Agent potrebbe non essere disinstallato. Analogamente, in cui Agent è già installato come parte del sistema operativo Windows, è possibile che il cabinet di installazione automatica dell'agente non venga installato.

Una volta installato, per chiamare le interfacce dell'agente, creare un'istanza del server e richiedere un puntatore a un'interfaccia specifica supportata dal server usando la convenzione COM standard. In particolare, la libreria COM fornisce una funzione API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), che crea un'istanza dell'oggetto e restituisce un puntatore all'interfaccia richiesta dell'oggetto. Richiedere un puntatore all'interfaccia [**IAgent**](iagent.md) o [**IAgentEx**](iagentex.md) nella chiamata **CoCreateInstance** o in una chiamata successiva a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

Il codice seguente illustra questo problema in C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Se il server Microsoft Agent è in esecuzione, questa funzione si connette al server. in caso contrario, viene avviato il server.

Si noti che le interfacce del server di Microsoft Agent includono spesso interfacce estese che includono un suffisso "ex". Queste interfacce sono derivate da e pertanto includono tutte le funzionalità di, le controparti non ex. Se si vuole usare una delle funzionalità estese, usare le interfacce ex.

Le funzioni che accettano i puntatori a BSTR allocano memoria usando [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). È responsabilità del chiamante liberare questa memoria usando [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring).

 

 
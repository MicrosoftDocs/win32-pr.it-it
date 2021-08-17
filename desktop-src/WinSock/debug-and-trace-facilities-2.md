---
description: Funzionalità di debug e traccia e Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Funzionalità di debug e traccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0617aa8fc18e90b0c3e366a7ab14f1457cb26471865bfcc97682801a858565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741368"
---
# <a name="debug-and-trace-facilities"></a>Funzionalità di debug e traccia

Windows Gli sviluppatori di applicazioni Sockets 2 devono isolare i bug in:

-   Applicazione.
-   *Ws232.dll\_* o una delle DLL shim di compatibilità.
-   Provider del servizio.

Windows Sockets 2 risolve questa esigenza tramite diversi componenti e funzionalità:

-   Supporto integrato per la traccia Winsock in Windows Vista e versioni successive.
-   Una versione di debug appositamente concepita di *Ws2 \_32.dll* in Windows Vista.
-   Una funzionalità di debug e traccia primitiva separata da usare in Windows Server 2003 e Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Traccia Winsock tramite Traccia eventi per Windows

Il supporto integrato per la traccia Winsock tramite Event Tracing for Windows (ETW) è incluso in Windows Vista e versioni successive. Questo è il metodo preferito per tracciare le chiamate Winsock Windows Vista e versioni successive. La traccia Winsock con ETW è leggera e funziona nelle versioni retail di Windows. Non sono necessari software o componenti aggiuntivi. Questa funzionalità deve essere abilitata solo in Windows Vista e versioni successive. Per informazioni più dettagliate, vedere gli argomenti relativi alla [traccia Winsock.](winsock-tracing.md)

## <a name="using-a-debug-version-of-ws2_32dll"></a>Uso di una versione di debug di Ws2 \_32.dll

La combinazione di una versione di debug del *\_32.dllWs2* in Windows Vista e la traccia Winsock consente di monitorare e controllare tutte le chiamate di procedura nell'API o spi di Windows Sockets 2.

Se una versione di Microsoft Windows Software Development Kit (SDK) per Windows Vista è installata nel percorso predefinito, le versioni di debug del *\_32.dllWs2* per diverse architetture si trovano nella cartella seguente:

**C: \\ Programmi Microsoft SDK Windows versione \\ \\ \\ 6.0 \\ NoRedist**

Deve essere usata una versione controllata del *\_32.dllWs2* corrispondente alla versione di Windows e al Service Pack in cui si sta testando. Tenere presente che potrebbero essere state applicate patch di sicurezza che hanno aggiornato l'32.dll *Ws2 \_* nel sistema di test. L Windows SDK per Windows Vista e le sottoscrizioni DVD/CD di Platform Software Development Kit (SDK) precedenti includono compilazioni controllate per le varie versioni di Windows. È consigliabile usare la stessa versione controllata del32.dll *Ws2 \_* della versione finale usata nel sistema sottoposto a test. Si noti anche che il comportamento in esecuzione in una compilazione controllata non sarà lo stesso dell'esecuzione con una compilazione di vendita al dettaglio.

**Nota**  L Windows SDK per Windows Server 2008 e versioni successive non include più versioni di debug speciali di *Ws2 \_32.dll*. Gli sviluppatori devono invece usare la traccia Winsock usando ETW, poiché questa funzionalità non richiede build di debug.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Funzionalità di debug e traccia di Winsock in Windows Server 2003 e Windows XP

Le versioni precedenti di Windows precedenti a Windows 8 e Windows Server 2012 supportano una funzionalità di debug e traccia primitiva separata inclusa come esempio con Windows SDK e Platform SDK precedente. La funzionalità di debug/traccia deve essere usata solo in Windows Server 2003 e Windows XP in cui la traccia Winsock non è supportata.

Se Windows SDK per Windows 7 è installato nel percorso predefinito, questa funzionalità di traccia Winsock primitiva viene installata nella cartella seguente:

**C: \\ Programmi Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock \\ dt \_ dll**

Il *DbgSpec.doc* file in questa cartella fornisce la documentazione su questa funzionalità di traccia primitiva. Per usare questa funzionalità, è necessario compilare il codice di esempio nella cartella \_ dt dll. Gli sviluppatori possono usare il codice sorgente per sviluppare versioni della DLL di debug/traccia che soddisfino le esigenze specifiche.

Si noti che questa funzionalità di traccia Winsock primitiva funzionerà solo con la versione di debug di *Ws2 \_32.dll* installata. Sarà quindi necessario ottenere una versione controllata del32.dll *Ws2 \_* corrispondente alla versione di Windows e al Service Pack su cui si sta testando.

Una limitazione di questa funzionalità di traccia dll dt primitiva è che il codice di esempio usa un blocco globale \_ (sezione critica) per ogni chiamata di funzione Winsock. Questa funzionalità non è quindi utile per gestire le race conditions. Il codice di esempio deve essere sostanzialmente riscritto per rendere questa funzionalità di traccia utile per gestire la maggior parte dei problemi reali di Winsock (sostituendo i blocchi globali). Questo codice di esempio consente agli sviluppatori di tracciare le chiamate di routine, i risultati delle procedure, i valori dei parametri e i valori restituiti.

Gli sviluppatori possono usare questo meccanismo primitivo per tracciare le chiamate di routine, i risultati delle procedure, i valori dei parametri e i valori restituiti. I valori dei parametri e i valori restituiti possono essere modificati alla chiamata di routine o alla restituzione della routine. Se lo si desidera, è possibile impedire o reindirizzare una chiamata di routine. Con l'accesso a questo livello di informazioni e controllo, uno sviluppatore è in grado di isolare meglio un problema nell'applicazione, nel *\_32.dllWs2* o nel provider di servizi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> </dl>

 

 




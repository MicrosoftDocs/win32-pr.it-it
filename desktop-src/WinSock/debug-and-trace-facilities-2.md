---
description: Funzionalità di debug e di traccia e Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Funzionalità di debug e di traccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288c6b4d72a7a375ee16da23a25b0a04a46df91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307001"
---
# <a name="debug-and-trace-facilities"></a>Funzionalità di debug e di traccia

Gli sviluppatori di applicazioni Windows Sockets 2 devono isolare i bug in:

-   Applicazione.
-   *Ws2 \_32.dll* o una delle DLL dello shim di compatibilità.
-   Provider del servizio.

Windows Sockets 2 risolve questa esigenza attraverso diversi componenti e funzionalità:

-   Supporto integrato per la traccia Winsock in Windows Vista e versioni successive.
-   Una versione di debug appositamente concepita di *Ws2 \_32.dll* in Windows Vista.
-   Una funzionalità di debug e traccia di primitiva separata per l'uso in Windows Server 2003 e Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Traccia Winsock con Event Tracing for Windows

Il supporto integrato per la traccia Winsock mediante Event Tracing for Windows (ETW) è incluso in Windows Vista e versioni successive. Si tratta del metodo preferito per la traccia delle chiamate Winsock in Windows Vista e versioni successive. La traccia Winsock con ETW è leggera e funziona con le versioni finali di Windows. Non sono richiesti software o componenti aggiuntivi. Questa funzionalità deve essere abilitata solo in Windows Vista e versioni successive. Per informazioni più dettagliate, vedere gli argomenti relativi alla [traccia Winsock](winsock-tracing.md) .

## <a name="using-a-debug-version-of-ws2_32dll"></a>Uso di una versione di debug di WS2 \_32.dll

La combinazione di una versione di debug di *Ws2 \_32.dll* in Windows Vista e della traccia Winsock consente il monitoraggio di tutte le chiamate di procedura tra l'API di Windows Sockets 2 o SPI e, a un certo punto, il controllo.

Se una versione di Microsoft Windows Software Development Kit (SDK) per Windows Vista è installata nel percorso predefinito, le versioni di debug di *Ws2 \_32.dll* per le varie architetture si trovano nella cartella seguente:

**C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ noredist**

Deve essere usata una versione controllata del *\_32.dllWS2* che corrisponde alla versione di Windows e al Service Pack su cui si sta eseguendo il test. Tenere presente che è possibile che siano state applicate patch di sicurezza che hanno aggiornato il *\_32.dllWS2* nel sistema di test. Il Windows SDK per Windows Vista e le sottoscrizioni DVD/CD (SDK) della piattaforma precedente includono compilazioni controllate per le varie versioni di Windows. È consigliabile usare la stessa versione controllata di *Ws2 \_32.dll* come versione definitiva usata nel sistema sottoposto a test. Si noti anche che il comportamento in esecuzione in una compilazione controllata non sarà uguale a quello dell'esecuzione con una build finale.

**Nota**  Il Windows SDK per Windows Server 2008 e versioni successive non include più versioni di debug speciali *della \_32.dllWS2*. Gli sviluppatori devono invece utilizzare la traccia Winsock utilizzando ETW, dal momento che questa funzionalità non richiede le build di debug.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Funzionalità di debug e traccia Winsock in Windows Server 2003 e Windows XP

Le versioni precedenti di Windows precedenti a Windows 8 e Windows Server 2012 supportano una funzionalità di debug e traccia della primitiva separata, inclusa come esempio con il Windows SDK e l'SDK della piattaforma precedente. La funzionalità debug/trace deve essere utilizzata solo in Windows Server 2003 e Windows XP, in cui la traccia Winsock non è supportata.

Se il Windows SDK per Windows 7 viene installato nel percorso predefinito, questa funzionalità di traccia di Winsock primitiva viene installata nella cartella seguente:

**C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ \\ dll Winsock DT \_**

Il file *DbgSpec.doc* in questa cartella fornisce la documentazione su questa funzionalità di traccia primitiva. \_Per usare questa funzionalità, è necessario compilare il codice di esempio nella cartella dll DT. Gli sviluppatori sono liberi di utilizzare il codice sorgente per sviluppare versioni della DLL di debug/traccia che soddisfano le proprie esigenze specifiche.

Si noti che questa funzionalità di traccia Winsock primitive funziona solo con la versione di debug di *Ws2 \_32.dll* installata. Sarà quindi necessario ottenere una versione controllata del *\_32.dllWS2* che corrisponda alla versione di Windows e al Service Pack su cui si sta eseguendo il test.

Una limitazione della funzionalità di traccia della DLL di DT primitiva \_ è che il codice di esempio usa un blocco globale (sezione critica) per ogni chiamata di funzione Winsock. Questa funzionalità non è quindi utile per la gestione delle race condition. Il codice di esempio deve essere riscritto in modo sostanziale per rendere questa funzionalità di traccia utile per gestire la maggior parte dei problemi reali di Winsock (sostituendo i blocchi globali). Questo codice di esempio consente agli sviluppatori di tracciare le chiamate di routine, le restituzioni delle procedure, i valori dei parametri e i valori restituiti.

Gli sviluppatori possono utilizzare questo meccanismo primitivo per tracciare le chiamate di routine, le restituzioni delle procedure, i valori dei parametri e i valori restituiti. I valori dei parametri e i valori restituiti possono essere modificati alla chiamata di routine o alla procedura restituita. Se lo si desidera, è possibile impedire o reindirizzare una chiamata di routine. Grazie all'accesso a questo livello di informazioni e controllo, uno sviluppatore è in grado di isolare in modo più efficace un problema nell'applicazione, *Ws2 \_32.dll* o provider di servizi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> </dl>

 

 




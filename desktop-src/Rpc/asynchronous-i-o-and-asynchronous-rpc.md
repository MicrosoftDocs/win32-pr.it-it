---
title: I/O asincrono e RPC asincrono
description: L'I/O asincrono è un mezzo efficace per un singolo thread per la gestione simultanea di più richieste di I/O.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932e85283eb67ff6675a646e791bbce5fe15d65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399603"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>I/O asincrono e RPC asincrono

L'I/O asincrono è un mezzo efficace per un singolo thread per la gestione simultanea di più richieste di I/O. La RPC asincrona sul server ha uno scopo simile per le richieste RPC. Nelle versioni di Windows precedenti a Windows Vista, l'invio di richieste di I/O asincrone dalle procedure del server mediante RPC asincrona è sconsigliato. Tuttavia, in Windows Vista e versioni successive di Windows, le richieste di I/O asincrone associate a una porta di completamento di I/O sono supportate da RPC asincrono.

Prima di Windows Vista, una chiamata di procedura remota asincrona può essere completata prima del completamento della richiesta di I/O asincrona. Quando la chiamata asincrona viene completata, il thread può terminare se il runtime RPC decide che è disponibile un numero sufficiente di thread per il servizio del carico di lavoro previsto. Il sistema associa tutte le richieste di I/O al thread che le avvia. Se il thread termina, eventuali richieste di I/O in sospeso su tale thread vengono interrotte. Le richieste I/O in sospeso non possono essere spostate in un altro thread.

Pertanto, le finestre di progettazione applicazioni destinate alle versioni di Windows precedenti a Windows Vista possono utilizzare l'I/O sincrono nelle procedure del server oppure possono inviare tutte le richieste che coinvolgono l'I/O asincrono alle procedure eseguite in un pool di thread gestito dall'applicazione. L'API Windows fornisce funzioni per la gestione dei pool di thread. Vedere [funzioni di processo e thread](/windows/desktop/ProcThread/process-and-thread-functions).

 

 
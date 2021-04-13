---
title: Modalità di archiviazione
description: L'archiviazione asincrona supporta due modalità di archiviazione bloccate e non bloccanti, che possono essere specificate da un client (un browser o l'oggetto stesso) restituendo BINDF \_ ASYNCSTORAGE dalla chiamata del moniker a IBindStatusCallback GetBindInfo..
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399442"
---
# <a name="storage-modes"></a>Modalità di archiviazione

L'archiviazione asincrona supporta due modalità di archiviazione: blocco e non blocco, che può essere specificato da un client (un browser o l'oggetto stesso) restituendo BINDF \_ ASYNCSTORAGE dalla chiamata del moniker a [**IBindStatusCallback:: GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Se un client specifica BINDF \_ ASYNCSTORAGE, riceve un puntatore a un archivio asincrono non bloccato. In caso contrario, riceve un puntatore a un archivio asincrono bloccante. Anche se il client non richiede un'operazione di associazione asincrona (non registrando [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con il contesto di associazione), il moniker restituisce ancora un archivio asincrono di blocco, abilitando il caricamento progressivo per le applicazioni legacy.

In modalità non di blocco, un'archiviazione asincrona restituisce E \_ in sospeso quando i dati non sono disponibili. Quando riceve questo messaggio, il client attende la notifica che sono disponibili dati aggiuntivi prima di riprovare a scaricarlo.

In modalità di blocco, anziché restituire E in \_ sospeso, l'archivio asincrono blocca la chiamata fino a quando non sono disponibili nuovi dati, quindi sblocca la chiamata e restituisce i nuovi dati. Il client deve essere pronto a ricevere i dati. Mentre il thread è bloccato, i dati già passati al client sono completamente disponibili per l'utente.

La modalità di blocco è necessaria perché i client ignari dell'archiviazione asincrona non riconoscono e \_ in sospeso e presuppone che si sia verificato un errore irreversibile. Il blocco dell'archiviazione asincrona consente ai client esistenti di eseguire il rendering progressivo.

 

 
---
title: Archiviazione Modalità
description: L'archiviazione asincrona supporta due modalità di archiviazione che bloccano e non bloccano, che un client (un browser o l'oggetto stesso) può specificare tramite la restituzione di BINDF ASYNCSTORAGE dalla chiamata del \_ moniker a IBindStatusCallback GetBindInfo.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a0a4c08daa1663f7513226dc25f4d5c8fd26341a6c8ee7d90a2ec0d1099db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661831"
---
# <a name="storage-modes"></a>Archiviazione Modalità

L'archiviazione asincrona supporta due modalità di archiviazione: blocco e non blocco, che un client (un browser o l'oggetto stesso) può specificare tramite la restituzione di BINDF ASYNCSTORAGE dalla chiamata del \_ moniker a [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Se un client specifica BINDF \_ ASYNCSTORAGE, riceve un puntatore a un archivio asincrono non bloccante. In caso contrario, riceve un puntatore a un'archiviazione asincrona di blocco. Anche se il client non richiede un'operazione di associazione asincrona (non [**registrando IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con il contesto di associazione), il moniker restituisce comunque un blocco dell'archiviazione asincrona, abilitando il caricamento progressivo per le applicazioni legacy.

In modalità non di blocco, un'archiviazione asincrona restituisce E \_ PENDING quando i dati non sono disponibili. Quando riceve questo messaggio, il client attende la notifica che sono disponibili dati aggiuntivi prima di riprovare a scaricarlo.

In modalità di blocco, invece di restituire E PENDING, l'archiviazione asincrona blocca la chiamata fino a quando non sono disponibili nuovi dati, quindi sblocca la chiamata e restituisce \_ i nuovi dati. Il client deve essere pronto a ricevere i dati. Mentre il thread è bloccato, i dati già passati al client sono completamente disponibili per l'utente.

La modalità di blocco è necessaria perché i client che non riconoscono l'archiviazione asincrona non riconosceranno E PENDING e presupporranno che si sia verificato un \_ errore irreversibile. Il blocco dell'archiviazione asincrona consente ai client esistenti di eseguire il rendering progressivo.

 

 
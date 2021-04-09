---
description: L'attraversamento della catena di attesa (WCT) consente ai debugger di diagnosticare blocchi e deadlock dell'applicazione.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Attraversamento della catena di attesa
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/04/2021
ms.locfileid: "103875890"
---
# <a name="wait-chain-traversal"></a>Attraversamento della catena di attesa

L'attraversamento della catena di attesa (WCT) consente ai debugger di diagnosticare blocchi e deadlock dell'applicazione.

Una *catena di attesa* è una sequenza alternata di thread e oggetti di sincronizzazione in cui ogni thread è in attesa dell'oggetto che segue. Ogni oggetto che segue, a sua volta, appartiene al thread successivo nella catena.

Un thread attende un oggetto di sincronizzazione dal momento in cui il thread richiede l'oggetto finché il thread non lo ha acquisito. Questo "blocco" è di proprietà di un thread a partire dal momento in cui il thread lo acquisisce, finché il thread non lo rilascia. In altre parole, quando il thread 1 è in attesa di un blocco di proprietà del thread 2, il thread 1 è "Waiting" per il thread 2.

WCT supporta le primitive di sincronizzazione seguenti:

- [Chiamata di procedura locale avanzata (ALPC)](../etw/alpc.md)
- [Component Object Model (COM)](../com/the-component-object-model.md)
- [Sezioni critiche](../sync/critical-section-objects.md)
- [Mutex](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- Operazioni di [attesa](../sync/wait-functions.md) su [processi e thread](../procthread/processes-and-threads.md)

Per recuperare la catena di attesa per uno o più thread, creare una sessione WCT usando le funzioni [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) e [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) . Le sessioni WCT sono rappresentate da un handle di tipo **HWCT**.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Le sessioni possono essere sincrone o asincrone

Le sessioni sincrone non possono essere annullate e bloccano il thread chiamante finché non viene recuperata una catena di attesa.

Le sessioni asincrone non bloccano il thread chiamante e possono essere annullate dall'applicazione mediante la funzione [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) . I risultati delle operazioni asincrone vengono resi disponibili tramite una funzione di callback [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) fornita dall'applicazione.

Per le sessioni asincrone, il chiamante può specificare un puntatore a una struttura di dati di contesto tramite [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (lo stesso puntatore viene passato alla funzione di callback [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).

La struttura dei dati di contesto è definita dall'utente e opaca per WCT. Può essere usato dall'applicazione per comunicare il contesto tra una query WCT e una funzione di callback. In genere, viene passato un handle di evento tramite questa struttura e, quando viene eseguito il callback, questo evento viene segnalato e un thread di monitoraggio viene informato che la query è stata completata.

Vedere [uso di WCT](using-wct.md) per un esempio di attraversamento della catena di attesa.

## <a name="related-topics"></a>Argomenti correlati

[Uso di WCT](using-wct.md), [riferimento a WCT](wct-reference.md), [MSDN Magazine 2007 luglio-Bugslayer: attraversamento della catena di attesa](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)
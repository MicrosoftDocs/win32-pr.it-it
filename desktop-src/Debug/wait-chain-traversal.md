---
description: Wait Chain Traversal (WCT) consente ai debugger di diagnosticare i blocchi e i deadlock dell'applicazione.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Attraversamento della catena di attesa
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 695e5298d0f56d0c53afcd146b19b1fc3c6ccf25e4ec12aec7f2b6b74fb64243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912311"
---
# <a name="wait-chain-traversal"></a>Attraversamento della catena di attesa

Wait Chain Traversal (WCT) consente ai debugger di diagnosticare i blocchi e i deadlock dell'applicazione.

Una *catena di attesa* è una sequenza alternata di thread e oggetti di sincronizzazione in cui ogni thread attende l'oggetto che segue. Ogni oggetto che segue è, a sua volta, di proprietà del thread successivo nella catena.

Un thread attende un oggetto di sincronizzazione dal momento in cui richiede l'oggetto fino a quando il thread non lo ha acquisito. Questo "blocco" è di proprietà di un thread dal momento in cui il thread lo acquisisce, fino a quando il thread lo rilascia. In altre parole, quando il thread 1 è in attesa di un blocco di proprietà del thread 2, il thread 1 è "in attesa" del thread 2.

WCT supporta le primitive di sincronizzazione seguenti:

- [Advanced Local Procedure Call (ALPC)](../etw/alpc.md)
- [Component Object Model (COM)](../com/the-component-object-model.md)
- [Sezioni critiche](../sync/critical-section-objects.md)
- [Mutex](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- [Operazioni](../sync/wait-functions.md) di attesa [su processi e thread](../procthread/processes-and-threads.md)

Per recuperare la catena di attesa per uno o più thread, creare una sessione WCT usando le funzioni [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) e [GetThreadWaitChain.](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) Le sessioni WCT sono rappresentate da un handle di **tipo HWCT.**

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Le sessioni possono essere sincrone o asincrone

Le sessioni sincrone non possono essere annullate e bloccare il thread chiamante finché non viene recuperata una catena di attesa.

Le sessioni asincrone non bloccano il thread chiamante e possono essere annullate dall'applicazione usando la [funzione CloseThreadWaitChainSession.](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) I risultati delle operazioni asincrone vengono resi disponibili tramite una funzione di callback [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) fornita dall'applicazione.

Per le sessioni asincrone, il chiamante può specificare un puntatore a una struttura di dati di contesto [tramite GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (questo stesso puntatore viene passato alla funzione di callback [WaitChainCallback).](/windows/win32/api/wct/nc-wct-pwaitchaincallback)

La struttura dei dati di contesto è definita dall'utente e opaca per WCT. Può essere usato dall'applicazione per comunicare il contesto tra una query WCT e una funzione di callback. In genere, si passa un handle di evento attraverso questa struttura e, quando viene eseguito il callback, questo evento viene segnalato e un thread di monitoraggio viene informato che la query è stata completata.

Vedere [Uso di WCT per](using-wct.md) un esempio di attraversamento della catena di attesa.

## <a name="related-topics"></a>Argomenti correlati

[Uso di WCT](using-wct.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 July - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)
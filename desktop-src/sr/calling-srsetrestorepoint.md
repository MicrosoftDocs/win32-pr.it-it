---
title: Chiamata di SRSetRestorePoint
description: Un'applicazione può creare un punto di ripristino prima di causare una modifica significativa del sistema, ad esempio un'installazione, una disinstallazione o un aggiornamento delle funzionalità.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592211"
---
# <a name="calling-srsetrestorepoint"></a>Chiamata di SRSetRestorePoint

Un'applicazione può creare un punto di ripristino prima di causare una modifica significativa del sistema, ad esempio un'installazione, una disinstallazione o un aggiornamento delle funzionalità.

I programmi di installazione devono creare un punto di ripristino subito prima dell'installazione chiamando la funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con il membro **dwEventType** della struttura [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) impostato su BEGIN \_ SYSTEM \_ CHANGE. Per notificare Ripristino configurazione di sistema'installazione è stata completata, chiamare **SRSetRestorePoint** con **dwEventType impostato** su END \_ SYSTEM \_ CHANGE.

Se l'utente annulla l'installazione dell'applicazione, il programma di installazione potrebbe rimuovere il punto di ripristino creato all'avvio dell'installazione. La rimozione del punto di ripristino è facoltativa e può impedire all'utente di eseguire il ripristino da modifiche non intenzionali apportate dal programma di installazione durante l'annullamento. Se il programma di installazione deve rimuovere un punto di ripristino, può chiamare la funzione [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) oppure [**chiamare SRSetRestorePoint con**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) **dwRestorePointType** impostato su CANCELLED OPERATION, dwEventType impostato su END SYSTEM CHANGE e llSequenceNumber impostato sul valore restituito dalla chiamata iniziale a \_  \_ \_ **SRSetRestorePoint.** 

**Windows 8: **

Una nuova chiave del Registro di sistema consente agli sviluppatori di applicazioni di modificare la frequenza di creazione del punto di ripristino.

Le applicazioni devono creare questa chiave per usarla perché non sarà preesistente nel sistema. Se la chiave non esiste, per impostazione predefinita verrà applicato quanto segue. Se un'applicazione chiama la **funzione SRSetRestorePoint** per creare un punto di ripristino, Windows ignora la creazione di questo nuovo punto di ripristino se sono stati creati punti di ripristino nelle ultime 24 ore. Ripristino configurazione di sistema imposta il membro **IISequenceNumber** della struttura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) sul numero di sequenza per il punto di ripristino creato in precedenza nel giorno e imposta il valore del membro **nStatus** su **ERROR \_ SUCCESS.** La **funzione SRSetRestorePoint** restituisce **TRUE.**

Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **SystemRestorePointCreationFrequency** nella chiave del Registro di sistema **HKLM \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ SystemRestore**. Il valore di questa chiave del Registro di sistema può modificare la frequenza di creazione del punto di ripristino. Il valore di questa chiave del Registro di sistema può modificare la frequenza di creazione del punto di ripristino.

Se l'applicazione chiama **SRSetRestorePoint** per creare un punto di ripristino e il valore della chiave del Registro di sistema è 0, il ripristino del sistema non ignora la creazione del nuovo punto di ripristino.

Se l'applicazione chiama **SRSetRestorePoint** per creare un punto di ripristino e il valore della chiave del Registro di sistema è il numero intero N, il ripristino del sistema ignora la creazione di un nuovo punto di ripristino se sono stati creati punti di ripristino nei precedenti N minuti.

**Windows 8: **

Ripristino configurazione di sistema in esecuzione Windows 8 monitora i file nel volume di avvio rilevanti solo per il ripristino del sistema. Gli snapshot del volume di avvio creato da Ripristino configurazione di sistema in esecuzione in Windows 8 possono essere eliminati se lo snapshot viene successivamente esposto da una versione precedente di Windows. Si noti che anche se è presente un solo volume di sistema, esiste un solo volume di avvio per ogni sistema operativo in un sistema ad avvio multiplo.

Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **ScopeSnapshots** nella chiave del Registro di sistema **HKLM \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ SystemRestore**. Se questo valore della chiave del Registro di sistema è 0, Ripristino configurazione di sistema gli snapshot del volume di avvio nello stesso modo delle versioni precedenti di Windows. Se questo valore viene eliminato, Ripristino configurazione di sistema in esecuzione in Windows 8 riprende la creazione di snapshot che monitorano i file nel volume di avvio rilevanti solo per il ripristino del sistema.

Per un esempio, vedere [Uso di Ripristino configurazione di sistema](using-system-restore.md).

 

 





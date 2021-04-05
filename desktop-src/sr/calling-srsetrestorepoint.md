---
title: Chiamata di SRSetRestorePoint
description: Un'applicazione può creare un punto di ripristino prima di causare una modifica significativa del sistema, ad esempio l'installazione, la disinstallazione o l'aggiornamento delle funzionalità.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b877c4fe73bcedad363bb4c9cc770a9638550dbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712982"
---
# <a name="calling-srsetrestorepoint"></a>Chiamata di SRSetRestorePoint

Un'applicazione può creare un punto di ripristino prima di causare una modifica significativa del sistema, ad esempio l'installazione, la disinstallazione o l'aggiornamento delle funzionalità.

I programmi di installazione devono creare un punto di ripristino subito prima dell'installazione chiamando la funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con il membro **dwEventType** del set di strutture [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) per iniziare la \_ modifica del sistema \_ . Per notificare a ripristino configurazione di sistema che l'installazione è stata completata, chiamare **SRSetRestorePoint** con **DWEVENTTYPE** impostato su Termina \_ modifica del sistema \_ .

Se l'utente annulla l'installazione dell'applicazione, il programma di installazione potrebbe rimuovere il punto di ripristino creato al momento dell'avvio dell'installazione. La rimozione del punto di ripristino è facoltativa e può impedire all'utente di eseguire il recupero da modifiche non intenzionali apportate dal programma di installazione durante l'annullamento. Se il programma di installazione prevede la rimozione di un punto di ripristino, può chiamare la funzione [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) oppure chiamare [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con **DWRESTOREPOINTTYPE** impostato su operazione annullata \_ , **DwEventType** impostato su Termina \_ \_ modifica del sistema e **llSequenceNumber** impostato sul valore restituito dalla chiamata iniziale a **SRSetRestorePoint**.

**Windows 8:  **

Una nuova chiave del registro di sistema consente agli sviluppatori di applicazioni di modificare la frequenza di creazione di punti di ripristino.

Le applicazioni devono creare questa chiave per utilizzarla perché non sarà preesistente nel sistema. Per impostazione predefinita, verranno applicati gli elementi seguenti se la chiave non esiste. Se un'applicazione chiama la funzione **SRSetRestorePoint** per creare un punto di ripristino, Windows ignora la creazione di questo nuovo punto di ripristino se sono stati creati punti di ripristino nelle ultime 24 ore. Ripristino configurazione di sistema imposta il membro **IISequenceNumber** della struttura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) sul numero di sequenza del punto di ripristino creato in precedenza nel giorno e imposta il valore del membro **nStatus** su **errore \_ riuscito**. La funzione **SRSetRestorePoint** restituisce **true**.

Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **SystemRestorePointCreationFrequency** nella chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino. Il valore di questa chiave del registro di sistema può modificare la frequenza di creazione del punto di ripristino.

Se l'applicazione chiama **SRSetRestorePoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è 0, ripristino configurazione di sistema non ignora la creazione del nuovo punto di ripristino.

Se l'applicazione chiama **SRSetRestorePoint** per creare un punto di ripristino e il valore della chiave del registro di sistema è Integer N, ripristino configurazione di sistema ignora la creazione di un nuovo punto di ripristino se sono stati creati punti di ripristino nei precedenti N minuti.

**Windows 8:  **

Ripristino configurazione di sistema in esecuzione in Windows 8 monitora i file del volume di avvio rilevanti solo per il ripristino del sistema. Gli snapshot del volume di avvio creato da ripristino configurazione di sistema in esecuzione in Windows 8 possono essere eliminati se lo snapshot viene successivamente esposto da una versione precedente di Windows. Si noti che anche se è presente un solo volume di sistema, esiste un volume di avvio per ogni sistema operativo in un sistema a più avvii.

Gli sviluppatori possono scrivere applicazioni che creano il valore **DWORD** **ScopeSnapshots** nella chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Se il valore della chiave del registro di sistema è 0, ripristino configurazione di sistema crea snapshot del volume di avvio nello stesso modo delle versioni precedenti di Windows. Se questo valore viene eliminato, ripristino configurazione di sistema in esecuzione in Windows 8 riprende la creazione di snapshot che monitorano i file del volume di avvio rilevanti solo per il ripristino del sistema.

Per un esempio, vedere [uso di ripristino configurazione di sistema](using-system-restore.md).

 

 





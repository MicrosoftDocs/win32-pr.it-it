---
description: Per consentire all'applicazione di usare Gestione sincronizzazione è necessario implementare un oggetto Component Object Model (COM) per gestire le notifiche di sincronizzazione ricevute da SyncMgr.
title: Uso di Gestione sincronizzazione da un programma
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11e959399624d30e1e6d7ce87fb8bb247de7c9c420ef9b2427c7b9bdeb00e7f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709381"
---
# <a name="using-synchronization-manager-from-a-program"></a>Uso di Gestione sincronizzazione da un programma

Per consentire all'applicazione di usare Gestione sincronizzazione è necessario implementare un oggetto Component Object Model (COM) per gestire le notifiche di sincronizzazione ricevute da SyncMgr. Il gestore dell'applicazione esegue la sincronizzazione per gli elementi gestiti. Incluso nel gestore, è necessario implementare [**l'interfaccia ISyncMgrSynchronize.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) È inoltre necessario fornire un oggetto enumeratore [**e ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) per tutti gli elementi separati che l'applicazione può sincronizzare.

SyncMgr implementa [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) e [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

SyncMgr chiama i metodi in [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) per ottenere informazioni sugli elementi che l'applicazione gestisce e informazioni sul gestore fornito per la sincronizzazione di questi elementi.

In fase di esecuzione, il processo di sincronizzazione segue questi passaggi.

1.  SyncMgr notifica all'applicazione che è il momento di eseguire la sincronizzazione per uno degli elementi che l'applicazione gestisce chiamando il metodo [**ISyncMgrSynchronize::Initialize.**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize)
2.  SyncMgr chiama [**ISyncMgrSynchronize::EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) per ottenere [**l'interfaccia ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) per gli elementi gestiti dall'applicazione.
3.  SyncMgr chiama [**ISyncMgrSynchronize::SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) per fornire al gestore il puntatore di interfaccia per [**l'interfaccia ISyncMgrSynchronizeCallback.**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) Il gestore usa questa interfaccia per chiamare di nuovo SyncMgr durante la sincronizzazione.
4.  SyncMgr chiama quindi il metodo [**ISyncMgrSynchronize::P repareForSync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) per offrire al gestore la possibilità di visualizzare qualsiasi elemento dell'interfaccia utente necessario prima dell'inizio della sincronizzazione. Ad esempio, un'applicazione di posta elettronica può visualizzare una finestra di dialogo di accesso utente.
5.  Il gestore chiama [**ISyncMgrSynchronizeCallback::EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) prima e dopo la visualizzazione degli elementi dell'interfaccia utente. Al termine, il gestore chiama [**ISyncMgrSynchronizeCallback::P repareForSyncCompleted.**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted)
6.  SyncMgr chiama il [**metodo ISyncMgrSynchronize::Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) per avviare la sincronizzazione.

Durante il processo di sincronizzazione, SyncMgr continua a chiamare metodi [**nell'interfaccia ISyncMgrSynchronize.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) Può inviare gli errori, lo stato di avanzamento e le notifiche del gestore. Può anche enumerare gli elementi che l'applicazione gestisce o consentire all'applicazione di visualizzare le proprietà per gli elementi.

Il gestore chiama i metodi in [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) per determinare se un elemento deve essere ignorato, per registrare gli errori e per registrare le informazioni sullo stato durante il processo di sincronizzazione.

Per altre informazioni, vedere le pagine di riferimento correlate per le interfacce coinvolte.

Al termine della sincronizzazione, il gestore chiama [**ISyncMgrSynchronizeCallback::SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 




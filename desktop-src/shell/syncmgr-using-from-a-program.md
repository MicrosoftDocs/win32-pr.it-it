---
description: Per consentire all'applicazione di utilizzare Gestione sincronizzazione, è necessario implementare un oggetto Component Object Model (COM) per gestire le notifiche di sincronizzazione ricevute da SyncMgr.
title: Utilizzo di gestione sincronizzazione da un programma
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9bd5abdc382c82c6c1aafcda3a967337384dc807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530175"
---
# <a name="using-synchronization-manager-from-a-program"></a>Utilizzo di gestione sincronizzazione da un programma

Per consentire all'applicazione di utilizzare Gestione sincronizzazione, è necessario implementare un oggetto Component Object Model (COM) per gestire le notifiche di sincronizzazione ricevute da SyncMgr. Il gestore dell'applicazione esegue la sincronizzazione per gli elementi gestiti. Incluso nel gestore, è necessario implementare l'interfaccia [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Inoltre, è necessario fornire un oggetto enumeratore e [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) per eventuali elementi distinti che l'applicazione può sincronizzare.

SyncMgr implementa [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) e [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

SyncMgr chiama i metodi in [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) per ottenere informazioni sugli elementi gestiti dall'applicazione e informazioni sul gestore fornito per la sincronizzazione di questi elementi.

In fase di esecuzione, il processo di sincronizzazione segue questa procedura.

1.  SyncMgr notifica all'applicazione che è il momento di eseguire la sincronizzazione per uno degli elementi gestiti dall'applicazione chiamando il metodo [**ISyncMgrSynchronize:: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) .
2.  SyncMgr chiama [**ISyncMgrSynchronize:: EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) per ottenere l'interfaccia [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) per gli elementi gestiti dall'applicazione.
3.  SyncMgr chiama [**ISyncMgrSynchronize:: SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) per fornire al gestore il puntatore di interfaccia per l'interfaccia [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) . Il gestore usa questa interfaccia per richiamare SyncMgr durante la sincronizzazione.
4.  SyncMgr chiama quindi il metodo [**ISyncMgrSynchronize::P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) per fornire al gestore la possibilità di visualizzare qualsiasi elemento dell'interfaccia utente necessario prima che inizi la sincronizzazione. Ad esempio, un'applicazione di posta elettronica può visualizzare una finestra di dialogo di accesso utente.
5.  Il gestore chiama [**ISyncMgrSynchronizeCallback:: EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) prima e dopo la visualizzazione di tutti gli elementi dell'interfaccia utente. Il gestore chiama [**ISyncMgrSynchronizeCallback::P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) al termine dell'operazione.
6.  SyncMgr chiama il metodo [**ISyncMgrSynchronize:: Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) per avviare la sincronizzazione.

Durante il processo di sincronizzazione, SyncMgr continua a chiamare i metodi nell'interfaccia [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Può inviare gli errori del gestore, lo stato di avanzamento e le notifiche. Può inoltre enumerare gli elementi gestiti dall'applicazione o consentire all'applicazione di visualizzare le proprietà degli elementi.

Il gestore chiama i metodi in [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) per determinare se un elemento deve essere ignorato, per registrare gli errori e per inviare informazioni sullo stato di avanzamento durante il processo di sincronizzazione.

Per ulteriori informazioni, vedere le pagine di riferimento correlate per le interfacce necessarie.

Al termine della sincronizzazione, il gestore chiama [**ISyncMgrSynchronizeCallback:: SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 




---
description: Sono disponibili diversi tipi di copia shadow che possono essere creati da un richiedente.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Creazione di copie shadow semplici per il backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751031"
---
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="1f739-103">Creazione di copie shadow semplici per il backup</span><span class="sxs-lookup"><span data-stu-id="1f739-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="1f739-104">Sono disponibili diversi tipi di copia shadow che possono essere creati da un richiedente.</span><span class="sxs-lookup"><span data-stu-id="1f739-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="1f739-105">Tuttavia, per la maggior parte delle applicazioni di backup, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f739-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="1f739-106">Chiamare [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con un contesto del \_ backup VSS CTX \_ .</span><span class="sxs-lookup"><span data-stu-id="1f739-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="1f739-107">Chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) per inizializzare la comunicazione con i writer.</span><span class="sxs-lookup"><span data-stu-id="1f739-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="1f739-108">Chiamare [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere componenti di file e database al backup.</span><span class="sxs-lookup"><span data-stu-id="1f739-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="1f739-109">Chiamare [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per inizializzare il meccanismo di copia shadow.</span><span class="sxs-lookup"><span data-stu-id="1f739-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="1f739-110">Chiamare [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) per includere i volumi nella copia shadow.</span><span class="sxs-lookup"><span data-stu-id="1f739-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="1f739-111">Chiamare [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) per notificare ai writer le operazioni di backup.</span><span class="sxs-lookup"><span data-stu-id="1f739-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 




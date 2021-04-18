---
description: "Durante un'operazione di ripristino, il richiedente può utilizzare il metodo IVssBackupComponents:: SetRestoreState per definire il tipo di operazione di ripristino in corso."
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: Stato ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307157"
---
# <a name="vss-restore-state"></a><span data-ttu-id="8f960-103">Stato ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="8f960-103">VSS Restore State</span></span>

<span data-ttu-id="8f960-104">Durante un'operazione di ripristino, il richiedente può utilizzare il metodo [**IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) per definire il tipo di operazione di ripristino in corso.</span><span class="sxs-lookup"><span data-stu-id="8f960-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="8f960-105">Tuttavia, per la maggior parte delle operazioni di ripristino non è necessario eseguire l'override del tipo di ripristino predefinito (VSS \_ RTYPE \_ undefined).</span><span class="sxs-lookup"><span data-stu-id="8f960-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="8f960-106">I writer devono considerare questo tipo di ripristino come se fosse VSS \_ RTYPE \_ per \_ copia.</span><span class="sxs-lookup"><span data-stu-id="8f960-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="8f960-107">Per ulteriori informazioni sui valori dei tipi di ripristino, vedere l'enumerazione del [**\_ \_ tipo di ripristino VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="8f960-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 




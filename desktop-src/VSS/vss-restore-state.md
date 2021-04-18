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
# <a name="vss-restore-state"></a>Stato ripristino VSS

Durante un'operazione di ripristino, il richiedente può utilizzare il metodo [**IVssBackupComponents:: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) per definire il tipo di operazione di ripristino in corso. Tuttavia, per la maggior parte delle operazioni di ripristino non è necessario eseguire l'override del tipo di ripristino predefinito (VSS \_ RTYPE \_ undefined). I writer devono considerare questo tipo di ripristino come se fosse VSS \_ RTYPE \_ per \_ copia. Per ulteriori informazioni sui valori dei tipi di ripristino, vedere l'enumerazione del [**\_ \_ tipo di ripristino VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 




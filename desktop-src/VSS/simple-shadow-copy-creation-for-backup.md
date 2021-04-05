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
# <a name="simple-shadow-copy-creation-for-backup"></a>Creazione di copie shadow semplici per il backup

Sono disponibili diversi tipi di copia shadow che possono essere creati da un richiedente. Tuttavia, per la maggior parte delle applicazioni di backup, è necessario eseguire le operazioni seguenti:

1.  Chiamare [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) con un contesto del \_ backup VSS CTX \_ .
2.  Chiamare [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) per inizializzare la comunicazione con i writer.
3.  Chiamare [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere componenti di file e database al backup.
4.  Chiamare [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) per inizializzare il meccanismo di copia shadow.
5.  Chiamare [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) per includere i volumi nella copia shadow.
6.  Chiamare [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) per notificare ai writer le operazioni di backup.

 

 




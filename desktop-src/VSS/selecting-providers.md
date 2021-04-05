---
description: Un richiedente deve selezionare un provider specifico solo se contiene alcune informazioni sui provider disponibili.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selezione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131255"
---
# <a name="selecting-providers"></a>Selezione di provider

Un richiedente deve selezionare un provider specifico solo se contiene alcune informazioni sui provider disponibili.

Poiché non si tratta in genere del caso, è consigliabile che un richiedente fornisca il GUID \_ null come ID provider a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), che consente al sistema di scegliere un provider secondo l'algoritmo seguente:

1.  Se è disponibile un provider hardware che supporta il volume specificato, viene selezionato.
2.  Se non è disponibile alcun provider hardware, viene selezionato se è disponibile un provider software specifico per il volume specificato.
3.  Se non è disponibile alcun provider hardware e nessun provider software specifico per i volumi, viene selezionato il provider di sistema.

Un richiedente può tuttavia ottenere informazioni sui provider disponibili usando [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Con queste informazioni e solo se l'applicazione di backup dispone di una conoscenza corretta dei diversi provider, un richiedente può fornire un ID provider valido a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Si noti che non è necessario che tutti i volumi abbiano lo stesso provider.

 

 




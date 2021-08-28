---
description: Un richiedente deve selezionare un provider specifico solo se dispone di alcune informazioni sui provider disponibili.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selezione dei provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2451f172a569a23ba4799c16f8598ade4e6fb011f051b7ba7d948c7a366f22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124501"
---
# <a name="selecting-providers"></a>Selezione dei provider

Un richiedente deve selezionare un provider specifico solo se dispone di alcune informazioni sui provider disponibili.

Poiché questo non è in genere il caso, è consigliabile che un richiedente fornisci GUID NULL come \_ ID provider a [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), che consente al sistema di scegliere un provider in base all'algoritmo seguente:

1.  Se è disponibile un provider hardware che supporta il volume specificato, viene selezionato.
2.  Se non è disponibile alcun provider hardware, viene selezionato se è disponibile un provider software specifico per il volume specificato.
3.  Se non è disponibile alcun provider hardware e nessun provider software specifico per i volumi, viene selezionato il provider di sistema.

Tuttavia, un richiedente può ottenere informazioni sui provider disponibili usando [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Con queste informazioni e solo se l'applicazione di backup ha una buona conoscenza dei vari provider, un richiedente può fornire un ID provider valido a [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Si noti che non tutti i volumi devono avere lo stesso provider.

 

 




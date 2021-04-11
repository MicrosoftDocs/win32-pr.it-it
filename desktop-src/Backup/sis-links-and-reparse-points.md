---
title: Collegamenti SIS e reparse point
description: SIS è un driver di filtro NTFS che sostituisce i file duplicati con i collegamenti copy-on-Write (detti collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Backup dei reparse point
- Backup dell'archivio a istanza singola (SIS), collegamenti SIS
- Backup dell'archivio a istanza singola (SIS), reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118211"
---
# <a name="sis-links-and-reparse-points"></a>Collegamenti SIS e reparse point

SIS è un driver di filtro NTFS che sostituisce i file duplicati con i collegamenti copy-on-Write (detti collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file. Questo file di backup è contenuto in un [archivio comune](the-sis-common-store-and-common-store-files.md). L'implementazione dell'architettura SIS usa i [reparse point](/windows/desktop/FileIO/reparse-points) contenenti informazioni sui collegamenti SIS.

I collegamenti SIS vengono implementati come file sparse, in genere con la maggior parte degli intervalli del file non allocato e un reparse point. La struttura e il contenuto di un punto di analisi è opaco per le applicazioni di backup e ripristino. Tuttavia, le applicazioni inviano e recuperano i dati all'interno di tali reparse point da e verso le funzioni API SIS che elaborano le informazioni in esse contenute. Le informazioni in un reparse point si riferiscono a un singolo file di backup che contiene i dati del file effettivi. Questo file di backup è denominato [file di archivio comune](the-sis-common-store-and-common-store-files.md)ed è presente nell'archivio comune.

Quando si ripristina un collegamento SIS, l'applicazione di ripristino deve eseguire i passaggi seguenti:

1.  Determinare il file o i file dell'archivio comune a cui punta il collegamento SIS.
2.  Se il file o i file non sono presenti nell'archivio comune, ripristinare il file o i file insieme al collegamento SIS.
3.  Se il collegamento SIS punta a un file o a un file di archivio comune esistente sul disco, ripristinare solo il collegamento SIS. Si ricordi che i dati nei file di archivio comuni non cambiano mai. Pertanto, se un file di archivio comune si trova ancora sul disco al momento del ripristino, avrà lo stesso contenuto del momento in cui è stato eseguito il backup e non è necessario sovrascriverlo.

L'unico overhead aggiuntivo necessario per i backup assistiti da SIS è che l'applicazione di backup deve eseguire il backup del collegamento SIS e dei dati associati ai file di supporto. Tutte le operazioni di backup e ripristino SIS sono locali in un volume specifico.

 

 
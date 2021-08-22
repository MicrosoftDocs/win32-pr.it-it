---
title: Collegamenti SIS e reparse point
description: SIS è un driver di filtro NTFS che sostituisce i file duplicati con collegamenti copy-on-write (denominati collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Reparse point Backup
- backup dell'archivio a istanza singola (SIS), collegamenti SIS
- backup dell'archivio a istanza singola (SIS), reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588861"
---
# <a name="sis-links-and-reparse-points"></a>Collegamenti SIS e reparse point

SIS è un driver di filtro NTFS che sostituisce i file duplicati con collegamenti copy-on-write (denominati collegamenti SIS) che puntano a un singolo file di backup, riducendo il sovraccarico del disco e della cache di tali file. Questo file di backup è contenuto in un [archivio comune.](the-sis-common-store-and-common-store-files.md) L'implementazione dell'architettura SIS usa [reparse point](/windows/desktop/FileIO/reparse-points) contenenti informazioni sui collegamenti SIS.

I collegamenti SIS vengono implementati come file sparse, in genere con la maggior parte degli intervalli del file non allocati e un reparse point. La struttura e il contenuto di un reparse point sono opachi per le applicazioni di backup e ripristino. Tuttavia, le applicazioni inviano e recuperano i dati all'interno di questi reparse point da e verso le funzioni dell'API SIS che elaborano le informazioni in essi contenute. Le informazioni in un reparse point fanno riferimento a un singolo file di backup che contiene i dati effettivi del file. Questo file di backup è denominato [file di archivio comune](the-sis-common-store-and-common-store-files.md)ed è presente nell'archivio comune.

Quando si ripristina un collegamento SIS, l'applicazione di ripristino deve eseguire i passaggi seguenti:

1.  Determinare il file o i file dell'archivio comune a cui punta il collegamento SIS.
2.  Se il file o i file non esistono nell'archivio comune, ripristinare il file o i file insieme al collegamento SIS.
3.  Se il collegamento SIS punta a uno o più file di archivio comune presenti sul disco, ripristinare solo il collegamento SIS. Tenere presente che i dati nei file di archivio comune non cambiano mai, quindi se un determinato file di archivio comune è ancora sul disco in fase di ripristino, ha lo stesso contenuto di quando è stato eseguito il backup e non è necessario sovrascriverlo.

L'unico sovraccarico aggiuntivo necessario per i backup assistiti da SIS è che l'applicazione di backup deve eseguire il backup del collegamento SIS e dei dati associati ai file di backup. Tutte le operazioni di backup e ripristino SIS sono locali in un volume specifico.

 

 
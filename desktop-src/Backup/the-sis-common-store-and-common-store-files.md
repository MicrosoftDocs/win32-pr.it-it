---
title: Archivio comune SIS e Common-Store file
description: Tutti i file di backup gestiti dal backup dell'archivio a istanza singola sono denominati file di archivio comune.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- backup di archivi comuni
- Backup dell'archivio a istanza singola (SIS), archivi comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19337a967fd858c149bc9d4261abc44214d4c76023abe022b5e1c5efd5f8ed3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529471"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Archivio comune SIS e Common-Store file

Tutti i file di backup gestiti dal backup dell'archivio a istanza singola sono denominati *file di archivio comune.* Un *archivio comune* esiste in ogni volume gestito da SIS e contiene tutti i file dell'archivio comune presenti in tale volume. Questa directory si trova nella directory radice del volume ed è denominata \\ "SIS Common Store". L'archivio comune viene implementato come directory protetta dal normale accesso utente, perché i file dell'archivio comune sono destinati a essere accessibili direttamente solo dalle funzioni API di backup SIS e non dalle applicazioni di backup e ripristino.

Le proprietà di un file di archivio comune sono le seguenti:

-   Un file di archivio comune può avere uno o più collegamenti che puntano a esso.
-   Dopo la creazione, il contenuto di un file di archivio comune non cambia mai.
-   I nomi dei file di archivio comune sono univoci a livello globale, ovvero sono univoci in tutti i volumi in tutti i sistemi del mondo e l'associazione tra un nome di file dell'archivio comune e i relativi dati è statica a livello globale.

Quando SIS è abilitato in un volume, viene quindi creata una copia dei file duplicati nell'archivio comune e tutti i file duplicati vengono sostituiti con collegamenti [SIS](sis-links-and-reparse-points.md) che puntano al file di archivio comune. Per altre informazioni, vedere [abilitazione o disabilitazione di SIS](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in un volume nella documentazione di TechNet.

Quando si accede a uno dei collegamenti SIS per un'operazione di scrittura, il filtro SIS ripristina innanzitutto il contenuto originale del file di collegamento SIS dal file di archivio comune, il reparse point che collega il file di collegamento SIS all'archivio comune viene rimosso e quindi l'operazione di scrittura viene eseguita sul file di destinazione originale.

Il file dell'archivio comune viene rimosso solo quando viene eliminato l'ultimo collegamento SIS che vi punta.

 

 
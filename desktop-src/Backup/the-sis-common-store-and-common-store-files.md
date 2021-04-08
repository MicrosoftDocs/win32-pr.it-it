---
title: Archivio comune SIS e file di Common-Store
description: Tutti i file di backup gestiti dal backup dell'archivio a istanza singola (SIS) sono denominati file di archivio comuni.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Backup di archivi comuni
- Backup dell'archivio a istanza singola (SIS), archivi comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872765"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Archivio comune SIS e file di Common-Store

Tutti i file di backup gestiti dal backup dell'archivio a istanza singola (SIS) sono denominati *file di archivio comuni*. Un *archivio comune* è presente in ogni volume gestito da SIS e contiene tutti i file di archivio comuni presenti in tale volume. Questa directory si trova nella directory radice del volume ed è denominata " \\ SIS Common Store". L'archivio comune viene implementato come una directory protetta da un accesso utente normale, perché i file di archivio comuni sono destinati all'accesso diretto solo alle funzioni API di backup SIS e non alle applicazioni di backup e ripristino.

Di seguito sono riportate le proprietà di un file di archivio comune:

-   Un file di archivio comune può includere uno o più collegamenti che vi fanno riferimento.
-   Una volta creato, il contenuto di un file di archivio comune non cambia mai.
-   I nomi dei file di archivio comuni sono univoci a livello globale, ovvero sono univoci in tutti i volumi in tutti i sistemi del mondo e il binding tra un nome di file di archivio comune e i relativi dati è statico a livello globale.

Quando SIS è abilitato in un volume, una copia dei file duplicati viene quindi creata nell'archivio comune e tutti i file duplicati vengono sostituiti con i [collegamenti SIS](sis-links-and-reparse-points.md) che puntano al file di archivio comune. Per ulteriori informazioni, vedere [Abilitazione o disabilitazione di SIS in un volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) nella documentazione di TechNet.

Quando si accede a uno dei collegamenti SIS per un'operazione di scrittura, il filtro SIS innanzitutto ripristina il contenuto originale del file di collegamento SIS dal file di archivio comune, il reparse point che collega il file di collegamento SIS all'archivio comune viene rimosso, quindi l'operazione di scrittura viene eseguita sul file di destinazione originale.

Il file di archivio comune viene rimosso solo quando l'ultimo collegamento SIS che punta a esso viene eliminato.

 

 
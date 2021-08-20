---
description: Descrive due tipi di limiti di quota del disco e come vengono misurati i limiti di quota del disco.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limiti di quota del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238b3068b49536867d733dfc858703a6001ff078bd99e383a9675bd6a52d038d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997859"
---
# <a name="disk-quota-limits"></a>Limiti di quota del disco

Lo spazio su disco utilizzato da ogni file viene addebitato direttamente all'utente proprietario del file. Il proprietario di un file è identificato dall'identificatore di sicurezza (SID) nelle informazioni di sicurezza per il file. Lo spazio totale su disco addebitato a un utente è la somma della lunghezza di tutti i flussi di dati. In altre parole, i flussi del set di proprietà e i flussi di dati utente residenti influiscono sulla quota dell'utente.

La quota non viene addebitata per i punti di analisi, i descrittori di sicurezza o altri metadati associati ai file. La compressione o la decompressione dei file non influisce sugli spazi su disco segnalati per i file. Di conseguenza, le impostazioni di quota in un volume possono essere confrontate con le impostazioni in un altro volume.

Esistono due tipi di limiti di quota del disco, come illustrato nella tabella seguente.



| Limite                        | Descrizione                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore soglia avvisi<br/> | È possibile configurare il sistema per generare una voce del file di log di sistema quando lo spazio su disco addebitato all'utente supera questo valore.<br/>                                                                                                                                         |
| Quota rigida<br/>        | È possibile configurare il sistema per generare una voce del file di log di sistema quando lo spazio su disco addebitato all'utente supera questo valore. È anche possibile configurare il sistema per negare spazio su disco aggiuntivo all'utente quando lo spazio su disco addebitato all'utente supera questo valore.<br/> |



 

L'file system NTFS crea automaticamente una voce di quota utente quando un utente scrive per la prima volta nel volume. Alle voci create automaticamente vengono assegnati i valori predefiniti di soglia di avviso e limite di quota rigida per il volume.

 

 





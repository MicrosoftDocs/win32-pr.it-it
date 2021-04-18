---
description: Descrive due tipi di limiti di quota del disco e il modo in cui vengono misurati i limiti delle quote del disco
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limiti della quota del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313889"
---
# <a name="disk-quota-limits"></a>Limiti della quota del disco

Lo spazio su disco utilizzato da ogni file viene addebitato direttamente all'utente proprietario del file. Il proprietario di un file è identificato dall'ID di sicurezza (SID) nelle informazioni di sicurezza per il file. Lo spazio totale su disco addebitato a un utente è la somma della lunghezza di tutti i flussi di dati. In altre parole, i flussi di set di proprietà e i flussi di dati utente residenti influiscono sulla quota dell'utente.

Per la quota non vengono addebitati punti di analisi, descrittori di sicurezza o altri metadati associati ai file. La compressione o la decompressione dei file non influisce sullo spazio su disco segnalato per i file. È pertanto possibile confrontare le impostazioni delle quote in un volume con le impostazioni di un altro volume.

Esistono due tipi di limiti di quota del disco, come illustrato nella tabella seguente.



| Limite                        | Descrizione                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore soglia avvisi<br/> | È possibile configurare il sistema in modo da generare una voce di registro di sistema quando lo spazio su disco addebitato all'utente supera questo valore.<br/>                                                                                                                                         |
| Quota rigida<br/>        | È possibile configurare il sistema in modo da generare una voce di registro di sistema quando lo spazio su disco addebitato all'utente supera questo valore. È inoltre possibile configurare il sistema in modo da negare ulteriore spazio su disco all'utente quando lo spazio su disco addebitato all'utente supera questo valore.<br/> |



 

Il file system NTFS crea automaticamente una voce di quota utente quando un utente scrive per la prima volta nel volume. Alle voci create automaticamente vengono assegnati la soglia di avviso predefinita e i valori di limite della quota hardware per il volume.

 

 





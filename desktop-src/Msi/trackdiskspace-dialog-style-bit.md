---
description: Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit di stile della finestra di dialogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810571"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Bit di stile della finestra di dialogo TrackDiskSpace

Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione. Se la proprietà viene modificata, invia una notifica ai controlli nella finestra di dialogo. Questo stile può essere usato se nella finestra di dialogo è presente un controllo che indica spazio su disco. Se l'utente passa a un'altra applicazione, aggiunge o rimuove file o modifica in altro modo lo spazio disponibile su disco, è possibile implementare rapidamente la modifica usando questo stile.

Qualsiasi finestra di dialogo basata sulla proprietà [**OutOfDiskSpace**](outofdiskspace.md) per determinare se visualizzare una finestra di dialogo deve impostare TrackDiskSpace Dialog Style Bit in modo che la finestra di dialogo aggiornerà dinamicamente lo spazio nei volumi di destinazione.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 




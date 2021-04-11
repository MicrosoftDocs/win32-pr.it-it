---
description: Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit di stile della finestra di dialogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128110"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Bit di stile della finestra di dialogo TrackDiskSpace

Se questo bit è impostato, la finestra di dialogo chiama periodicamente il programma di installazione. Se la proprietà viene modificata, viene inviata una notifica ai controlli della finestra di dialogo. Questo stile può essere utilizzato se è presente un controllo nella finestra di dialogo che indica lo spazio su disco. Se l'utente passa a un'altra applicazione, aggiunge o rimuove file o modifica in altro modo lo spazio su disco disponibile, è possibile implementare rapidamente la modifica usando questo stile.

Qualsiasi finestra di dialogo che si basa sulla proprietà [**OutOfDiskSpace**](outofdiskspace.md) per determinare se visualizzare una finestra di dialogo deve impostare il bit di stile della finestra di dialogo TrackDiskSpace per la finestra di dialogo per aggiornare in modo dinamico lo spazio sui volumi di destinazione.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 




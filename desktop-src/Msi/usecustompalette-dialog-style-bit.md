---
description: Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con la tavolozza personalizzata (una per finestra di dialogo ricevuta dal primo controllo creato). Se il bit non è impostato, il rendering delle immagini viene eseguito utilizzando una tavolozza predefinita.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit di stile della finestra di dialogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318981"
---
# <a name="usecustompalette-dialog-style-bit"></a>Bit di stile della finestra di dialogo UseCustomPalette

Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con la tavolozza personalizzata (una per finestra di dialogo ricevuta dal primo controllo creato). Se il bit non è impostato, il rendering delle immagini viene eseguito utilizzando una tavolozza predefinita.

In genere si imposta questo bit se la finestra di dialogo contiene un'immagine con una tavolozza speciale o diverse immagini che condividono una tavolozza personalizzata. Non impostare il bit se la finestra di dialogo contiene diverse immagini con tavolozze diverse. In questo caso, è più probabile che la tavolozza predefinita fornisca un risultato soddisfacente per tutte le immagini.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 




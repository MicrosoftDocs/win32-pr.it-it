---
description: Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con il riquadro personalizzato (uno per ogni finestra di dialogo ricevuta dal primo controllo creato). Se il bit non è impostato, il rendering delle immagini viene eseguito usando una tavolozza predefinita.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit di stile della finestra di dialogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9863f9b20ad85caf3712c3cfa00fd88de72f82b947a329d367d06f02ba06163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809481"
---
# <a name="usecustompalette-dialog-style-bit"></a>Bit di stile della finestra di dialogo UseCustomPalette

Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con il riquadro personalizzato (uno per ogni finestra di dialogo ricevuta dal primo controllo creato). Se il bit non è impostato, il rendering delle immagini viene eseguito usando una tavolozza predefinita.

In genere questo bit viene impostato se la finestra di dialogo contiene un'immagine con una tavolozza speciale o più immagini che condividono una tavolozza personalizzata. Il bit non deve essere impostato se la finestra di dialogo contiene diverse immagini con tavolozze diverse. In questo caso, è molto probabile che il riquadro predefinito dia un risultato soddisfacente per tutte le immagini.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 




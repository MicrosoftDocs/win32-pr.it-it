---
description: Se questo bit è impostato, il testo nel controllo viene visualizzato su una singola riga. Se il testo si estende oltre i margini del controllo, viene troncato e i puntini di sospensione (&\# 0034;...&\# 0034;) viene inserito alla fine per indicare il troncamento. Se questo bit non è impostato, il testo va a capo.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attributo del controllo NoWrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ef67a58dd0898b4c1e6d1577d35d67e8810649d49425087fecc3e0b3518cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519641"
---
# <a name="nowrap-control-attribute"></a>Attributo del controllo NoWrap

Se questo bit è impostato, il testo nel controllo viene visualizzato su una singola riga. Se il testo si estende oltre i margini del controllo, viene troncato e alla fine vengono inseriti i puntini di sospensione ("...") per indicare il troncamento. Se questo bit non è impostato, il testo va a capo.

## <a name="valid-controls"></a>Controlli validi

[Text](text-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere il bit NoWrap nella colonna Attributes del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo.](controls.md)

 

 




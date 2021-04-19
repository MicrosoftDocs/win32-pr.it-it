---
description: Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di comando, ma la logica rimane invariata. Se il bit non è impostato, i controlli vengono disegnati nello stile usuale.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Attributo di controllo PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311723"
---
# <a name="pushlike-control-attribute"></a>Attributo di controllo PushLike

Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di comando, ma la logica rimane invariata. Se il bit non è impostato, i controlli vengono disegnati nello stile usuale.

## <a name="valid-controls"></a>Controlli validi

[Casella](checkbox-control.md)di controllo[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit PushLike nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 




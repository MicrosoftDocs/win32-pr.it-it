---
description: Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di pressione, ma la relativa logica rimane la stessa. Se il bit non è impostato, i controlli vengono disegnati nello stile consueto.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Attributo del controllo PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692480"
---
# <a name="pushlike-control-attribute"></a>Attributo del controllo PushLike

Se questo bit è impostato su una casella di controllo o un gruppo di pulsanti di opzione, il pulsante viene disegnato con l'aspetto di un pulsante di pressione, ma la relativa logica rimane la stessa. Se il bit non è impostato, i controlli vengono disegnati nello stile consueto.

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit PushLike nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo](controls.md).

 

 




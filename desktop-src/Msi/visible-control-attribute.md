---
description: Se il bit Visible Control è impostato, il controllo è visibile nella finestra di dialogo. Se questo bit non è impostato, il controllo viene nascosto nella finestra di dialogo. Lo stato visibile o nascosto dell'attributo visible del controllo può essere modificato in un secondo momento da un evento di controllo.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Attributo visible control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abdecdc46f179b7639a6ecaa627d92b643ed781ade242a152262d38c46f7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498801"
---
# <a name="visible-control-attribute"></a>Attributo visible control

Se il bit Visible Control è impostato, il controllo è visibile nella finestra di dialogo. Se questo bit non è impostato, il controllo viene nascosto nella finestra di dialogo. Lo stato visibile o nascosto dell'attributo del controllo Visible può essere modificato in un secondo momento da un [evento di controllo](control-events.md).

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Commenti

È possibile usare la [tabella ControlCondition](controlcondition-table.md) per visualizzare o nascondere un controllo in base al valore di una proprietà o di un'istruzione condizionale. È anche possibile visualizzare o nascondere un controllo sottoscrivendo il controllo a [un oggetto ControlEvent.](control-events.md) Immettere l'identificatore dell'attributo nella colonna Attributo e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo.](controls.md)

 

 




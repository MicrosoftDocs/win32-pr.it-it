---
description: Questo attributo specifica se il controllo specificato è abilitato o disabilitato. La maggior parte dei controlli viene visualizzata in grigio quando è disabilitata.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Attributo del controllo Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40de14ac0205c52cce46c6050de0282e62df90d50f3bcdeb576771c9107ffc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763921"
---
# <a name="enabled-control-attribute"></a>Attributo del controllo Enabled

Questo attributo specifica se il controllo specificato è abilitato o disabilitato. La maggior parte dei controlli viene visualizzata in grigio quando è disabilitata.

Se questo bit è impostato, il controllo viene creato come abilitato.

Se questo bit non è impostato, il controllo viene creato come disabilitato.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli. L'impostazione di questo attributo non ha alcun effetto sull'aspetto di alcuni controlli non associati a una proprietà, ad esempio bitmap e icone.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Commenti

È anche possibile usare la [tabella ControlCondition per](controlcondition-table.md) disabilitare o abilitare un controllo in base al valore di una proprietà o di un'istruzione condizionale.

È anche possibile abilitare o disabilitare un controllo sottoscrivendo il controllo a [un oggetto ControlEvent.](control-events.md) Immettere l'identificatore dell'attributo nella colonna Attributo e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 




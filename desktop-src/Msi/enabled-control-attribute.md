---
description: Questo attributo specifica se il controllo specificato è abilitato o disabilitato. La maggior parte dei controlli è grigio quando è disabilitata.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Attributo di controllo abilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309488"
---
# <a name="enabled-control-attribute"></a>Attributo di controllo abilitato

Questo attributo specifica se il controllo specificato è abilitato o disabilitato. La maggior parte dei controlli è grigio quando è disabilitata.

Se questo bit è impostato, il controllo viene creato come abilitato.

Se questo bit non è impostato, il controllo viene creato come disabilitato.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli. L'aspetto di alcuni controlli che non sono associati a una proprietà, ad esempio bitmap e icone, non è influenzato dall'impostazione di questo attributo.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Commenti

È anche possibile usare la [tabella ControlCondition](controlcondition-table.md) per disabilitare o abilitare un controllo in base al valore di una proprietà o di un'istruzione condizionale.

È anche possibile abilitare o disabilitare un controllo sottoscrivendo il controllo a un [ControlEvent](control-events.md). Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 




---
description: Se questo bit è impostato, il controllo viene visualizzato con un aspetto tridimensionale incassato.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Attributo di controllo incassato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3547f06d82a66a08a575958eac728051c3315f3382529065c3792cfdb94def
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626931"
---
# <a name="sunken-control-attribute"></a>Attributo di controllo incassato

Se questo bit è impostato, il controllo viene visualizzato con un aspetto tridimensionale incassato. L'effetto di questo bit di stile è diverso su diversi controlli e versioni di Windows. In alcuni controlli non ha alcun effetto visibile. Se il sistema non supporta l'attributo del controllo Incassato, il controllo viene visualizzato nello stile di visualizzazione predefinito. Se questo bit non è impostato, il controllo viene visualizzato con lo stile di visualizzazione predefinito.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo , includere il bit incassato nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo.](controls.md)

 

 




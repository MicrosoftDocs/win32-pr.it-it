---
description: Se questo bit è impostato, il controllo viene visualizzato con un aspetto incassato a tre dimensioni.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Attributo di controllo incassato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130274"
---
# <a name="sunken-control-attribute"></a>Attributo di controllo incassato

Se questo bit è impostato, il controllo viene visualizzato con un aspetto incassato a tre dimensioni. L'effetto di questo bit di stile è diverso per i diversi controlli e versioni di Windows. In alcuni controlli non ha alcun effetto visibile. Se il sistema non supporta l'attributo di controllo incassato, il controllo viene visualizzato nello stile di visualizzazione predefinito. Se questo bit non è impostato, il controllo viene visualizzato con lo stile di visualizzazione predefinito.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit incassato nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 




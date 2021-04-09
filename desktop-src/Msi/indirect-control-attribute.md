---
description: L'attributo di controllo indiretto specifica se viene fatto riferimento indirettamente al valore visualizzato o modificato da questo controllo.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Attributo di controllo indiretto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d0c183f586c197b14810e7176bce607ac3adaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880866"
---
# <a name="indirect-control-attribute"></a>Attributo di controllo indiretto

L'attributo di controllo indiretto specifica se viene fatto riferimento indirettamente al valore visualizzato o modificato da questo controllo. Se questo bit è impostato, il controllo Visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna proprietà della [tabella dei controlli](control-table.md). Se questo bit non è impostato, il controllo Visualizza o modifica il valore della proprietà nella colonna proprietà della tabella dei controlli.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli attivi.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Commenti

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 




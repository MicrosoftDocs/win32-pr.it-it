---
description: L'attributo Del controllo indiretto specifica se al valore visualizzato o modificato da questo controllo viene fatto riferimento indirettamente.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Attributo del controllo indiretto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c679938a818fb8393958c35694f3c2b7f782c91fc2dfcf1ac04777553ec629c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996689"
---
# <a name="indirect-control-attribute"></a>Attributo del controllo indiretto

L'attributo Del controllo indiretto specifica se al valore visualizzato o modificato da questo controllo viene fatto riferimento indirettamente. Se questo bit è impostato, il controllo visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna Proprietà della [tabella Control](control-table.md). Se questo bit non è impostato, il controllo visualizza o modifica il valore della proprietà nella colonna Proprietà della tabella Control.

## <a name="valid-controls"></a>Controlli validi

Tutti i controlli attivi.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Commenti

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 




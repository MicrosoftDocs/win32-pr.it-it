---
description: La proprietà di sola lettura dipendenze dell'oggetto merge restituisce una raccolta di oggetti dipendenza che enumera un set di dipendenze non soddisfatte per il database corrente.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Proprietà merge. dipendenze (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327806"
---
# <a name="mergedependencies-property"></a>Merge. dipendenze (proprietà)

La proprietà di sola lettura **dipendenze** dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**dipendenza**](dependency-object.md) che enumera un set di dipendenze non soddisfatte per il database corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Non è necessario che un modulo sia aperto per recuperare le informazioni sulle dipendenze.

### <a name="c"></a>C++

Vedere ottenere la funzione delle [**\_ dipendenze**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

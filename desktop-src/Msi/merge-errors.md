---
description: La proprietà errori di sola lettura dell'oggetto merge restituisce una raccolta di oggetti Error che rappresenta il set di errori corrente.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Proprietà merge. Errors (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327804"
---
# <a name="mergeerrors-property"></a>Merge. Errors (proprietà)

La proprietà **errori** di sola lettura dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**Error**](error-object.md) che rappresenta il set di errori corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il recupero non è distruttivo. È possibile recuperare più istanze della raccolta Error chiamando ripetutamente questo metodo.

### <a name="c"></a>C++

Vedere la funzione [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 

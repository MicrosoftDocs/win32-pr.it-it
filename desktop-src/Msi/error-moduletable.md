---
description: La proprietà ModuleTable di sola lettura restituisce il nome della tabella nel modulo che ha causato l'errore.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Proprietà Error. ModuleTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326385"
---
# <a name="errormoduletable-property"></a>Proprietà Error. ModuleTable

La proprietà **ModuleTable** di sola lettura restituisce il nome della tabella nel modulo che ha causato l'errore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La raccolta è vuota se i valori non sono validi per il tipo di errore. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) la funzione ModuleTable.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 


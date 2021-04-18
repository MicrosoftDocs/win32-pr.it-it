---
description: La proprietà DatabaseTable di sola lettura dell'oggetto Error restituisce il nome della tabella nel database che ha causato l'errore.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Proprietà Error. DatabaseTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324244"
---
# <a name="errordatabasetable-property"></a>Proprietà Error. DatabaseTable

La proprietà **DatabaseTable** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce il nome della tabella nel database che ha causato l'errore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La raccolta è vuota se i valori non sono validi per il tipo di errore. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) la funzione DatabaseTable.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 


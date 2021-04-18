---
description: La proprietà DatabaseKeys di sola lettura dell'oggetto Error restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che hanno causato l'errore. È presente una chiave per ogni voce nella raccolta.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Proprietà Error. DatabaseKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324245"
---
# <a name="errordatabasekeys-property"></a>Proprietà Error. DatabaseKeys

La proprietà **DatabaseKeys** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che hanno causato l'errore. È presente una chiave per ogni voce nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il client è responsabile del rilascio della raccolta di stringhe quando non è più necessario.

La raccolta è vuota se i valori non sono validi per il tipo di errore. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) la funzione DatabaseKeys.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 


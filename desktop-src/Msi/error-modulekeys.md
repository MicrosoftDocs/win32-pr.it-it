---
description: La proprietà ModuleKeys di sola lettura dell'oggetto Error restituisce un puntatore a una raccolta di stringhe contenente le chiavi primarie della riga nel modulo che causa l'errore, una chiave per ogni voce della raccolta.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Proprietà Error. ModuleKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326386"
---
# <a name="errormodulekeys-property"></a>Proprietà Error. ModuleKeys

La proprietà **ModuleKeys** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce un puntatore a una raccolta di stringhe contenente le chiavi primarie della riga nel modulo che causa l'errore, una chiave per ogni voce della raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il client è responsabile del rilascio della raccolta di stringhe quando non è più necessario.

La raccolta è vuota se i valori non sono validi per il tipo di errore. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) la funzione ModuleKeys.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 


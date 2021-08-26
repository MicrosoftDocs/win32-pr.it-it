---
description: La proprietà DatabaseKeys di sola lettura dell'oggetto Error restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che causa l'errore. Nella raccolta è presente una chiave per ogni voce.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Proprietà Error.DatabaseKeys (Mergemod.h)
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
ms.openlocfilehash: 075fba028dd045c831adb84a7133fd524398fc74037b7e3c31116b76a4c95a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086041"
---
# <a name="errordatabasekeys-property"></a>Proprietà Error.DatabaseKeys

La proprietà **DatabaseKeys di** sola lettura dell'oggetto [**Error**](error-object.md) restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che causa l'errore. Nella raccolta è presente una chiave per ogni voce.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il client è responsabile del rilascio della raccolta di stringhe quando non è più necessaria.

La raccolta è vuota se i valori non si applicano al tipo di errore. È possibile determinare il tipo di errore chiamando la [**proprietà Type**](error-type.md) dell'oggetto [**Error.**](error-object.md)

### <a name="c"></a>C++

Vedere [**la funzione get \_ DatabaseKeys.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 


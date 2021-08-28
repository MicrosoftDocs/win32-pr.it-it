---
description: Scarica la cache di compatibilità dell'applicazione.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: Funzione BaseFlushAppcompatCache
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 44ea71a28ff85b00c72dc7b0255144381a2d8f01ead0901ee30ff216e17e20d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768751"
---
# <a name="baseflushappcompatcache-function"></a>Funzione BaseFlushAppcompatCache

Scarica la cache di compatibilità dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE se** ha esito positivo e FALSE in **caso contrario.**

## <a name="remarks"></a>Commenti

Il chiamante deve essere un amministratore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShimFlushCache**](shimflushcache.md)
</dt> </dl>

 

 





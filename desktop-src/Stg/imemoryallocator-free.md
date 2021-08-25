---
title: Metodo IMemoryAllocator Free
description: Il metodo Free libera la memoria allocata dal metodo Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Metodo gratuito Structured Archiviazione
- Metodo gratuito Structured Archiviazione, interfaccia IMemoryAllocator
- Interfaccia IMemoryAllocator strutturata Archiviazione metodo , Free
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906171"
---
# <a name="imemoryallocatorfree-method"></a>Metodo IMemoryAllocator::Free

Il **metodo Free** libera la memoria allocata dal metodo [**Allocate.**](imemoryallocator-allocate.md)

## <a name="syntax"></a>Sintassi


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pv* 
</dt> <dd>

Puntatore alla memoria da liberare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

 






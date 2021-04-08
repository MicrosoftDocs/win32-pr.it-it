---
title: Metodo gratuito IMemoryAllocator
description: Il metodo Free libera la memoria allocata dal metodo allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Archiviazione strutturata metodo gratuito
- Archiviazione strutturata di metodi gratuiti, interfaccia IMemoryAllocator
- Archiviazione strutturata dell'interfaccia IMemoryAllocator, metodo gratuito
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
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047962"
---
# <a name="imemoryallocatorfree-method"></a>Metodo IMemoryAllocator:: Free

Il metodo **Free** libera la memoria allocata dal metodo [**allocate**](imemoryallocator-allocate.md) .

## <a name="syntax"></a>Sintassi


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PV* 
</dt> <dd>

Puntatore alla memoria da liberare.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 






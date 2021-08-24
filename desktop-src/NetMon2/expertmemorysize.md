---
description: La funzione ExpertMemorySize restituisce la quantità di memoria allocata dalla funzione ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Funzione ExpertMemorySize (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744271"
---
# <a name="expertmemorysize-function"></a>Funzione ExpertMemorySize

La **funzione ExpertMemorySize** restituisce la quantità di memoria allocata dalla [funzione ExpertAllocMemory.](expertallocmemory.md)

## <a name="syntax"></a>Sintassi


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione](run.md) Run.

</dd> <dt>

*pOriginalMemory* \[ Pollici\]
</dt> <dd>

Puntatore all'indirizzo di memoria dell'esperto allocato [da ExpertAllocMemory.](expertallocmemory.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce la quantità di memoria allocata in byte.

## <a name="remarks"></a>Commenti

Per informazioni sul **tipo di dati SIZE \_ T** restituito **da ExpertMemorySize,** vedere Tipi di dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





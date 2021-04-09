---
description: La funzione ExpertMemorySize restituisce la quantità di memoria allocata dalla funzione ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Funzione ExpertMemorySize (Netmon. h)
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
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878662"
---
# <a name="expertmemorysize-function"></a>ExpertMemorySize (funzione)

La funzione **ExpertMemorySize** restituisce la quantità di memoria allocata dalla funzione [ExpertAllocMemory](expertallocmemory.md) .

## <a name="syntax"></a>Sintassi


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .

</dd> <dt>

*pOriginalMemory* \[ in\]
</dt> <dd>

Puntatore all'indirizzo di memoria dell'esperto allocato da [ExpertAllocMemory](expertallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce la quantità di memoria allocata in byte.

## <a name="remarks"></a>Commenti

Per informazioni sul tipo di dati **size \_ T** restituito da **ExpertMemorySize** , vedere tipi di dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





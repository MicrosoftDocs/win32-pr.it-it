---
description: Creare una pompa di thread.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Funzione D3DX10CreateThreadPump (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969475"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump (funzione)

Creare una pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cIoThreads* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di thread I/O da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*cProcThreads* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di thread di processo da creare. Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

Pompa di thread creata. Vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Una pompa di thread è un oggetto con utilizzo intensivo delle risorse. Per ogni applicazione è necessario creare solo un thread pump.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

---
description: Ottenere il numero di elementi in ognuna delle tre code all'interno della pompa di thread.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'Metodo ID3DX10ThreadPump:: GetQueueStatus (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323672"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a>Metodo ID3DX10ThreadPump:: GetQueueStatus

Ottenere il numero di elementi in ognuna delle tre code all'interno della pompa di thread.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIoQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di elementi nella coda di I/O.

</dd> <dt>

*pProcessQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di elementi nella coda dei processi.

</dd> <dt>

*pDeviceQueue* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di elementi nella coda del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

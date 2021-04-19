---
description: Restituisce un handle di evento per l'evento attualmente in esecuzione sulla traccia di animazione specificata.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Metodo ID3DXAnimationController:: GetCurrentTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323174"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>Metodo ID3DXAnimationController:: GetCurrentTrackEvent

Restituisce un handle di evento per l'evento attualmente in esecuzione sulla traccia di animazione specificata.

## <a name="syntax"></a>Sintassi


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore di traccia.

</dd> <dt>

*EventType* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXEVENT \_**](./d3dxevent-type.md)**

Tipo di evento su cui eseguire una query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento attualmente in esecuzione nella traccia specificata. Se non è in esecuzione alcun evento nella traccia specificata, viene restituito **null** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

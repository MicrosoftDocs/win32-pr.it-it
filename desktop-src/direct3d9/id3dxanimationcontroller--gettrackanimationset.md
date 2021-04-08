---
description: Ottiene il set di animazioni per la traccia specificata.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'Metodo ID3DXAnimationController:: GetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969424"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a>Metodo ID3DXAnimationController:: GetTrackAnimationSet

Ottiene il set di animazioni per la traccia specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore di traccia.

</dd> <dt>

*ppAnimSet* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) per la traccia specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

---
description: Imposta il peso della traccia. Il peso viene usato per determinare come unire più tracce.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'Metodo ID3DXAnimationController:: SetTrackWeight (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762364"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a>Metodo ID3DXAnimationController:: SetTrackWeight

Imposta il peso della traccia. Il peso viene usato per determinare come unire più tracce.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia su cui impostare il peso.

</dd> <dt>

*Peso* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore del peso.

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

 

 

---
description: Applica il set di animazioni alla traccia specificata.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Metodo ID3DXAnimationController:: SetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323284"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>Metodo ID3DXAnimationController:: SetTrackAnimationSet

Applica il set di animazioni alla traccia specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore della traccia a cui viene applicato il set di animazioni.

</dd> <dt>

*pAnimSet* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) da aggiungere alla traccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo imposta il set di animazioni sulla traccia specificata per la combinazione. Il set di animazioni per ogni traccia viene mescolato in base al peso e alla velocità della traccia quando viene chiamato [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

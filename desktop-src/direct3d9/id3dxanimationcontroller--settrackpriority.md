---
description: Imposta il peso della combinazione di priorità per la traccia di animazione specificata.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Metodo ID3DXAnimationController:: SetTrackPriority (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323642"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>Metodo ID3DXAnimationController:: SetTrackPriority

Imposta il peso della combinazione di priorità per la traccia di animazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore di traccia.

</dd> <dt>

*Priorità* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**

Tenere traccia della priorità. Questo parametro deve essere impostato su una delle costanti dal [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

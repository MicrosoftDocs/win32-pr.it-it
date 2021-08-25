---
description: Imposta lo spessore di fusione della priorità per la traccia di animazione specificata.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: Metodo ID3DXAnimationController::SetTrackPriority (D3dx9anim.h)
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
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848971"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>Metodo ID3DXAnimationController::SetTrackPriority

Imposta lo spessore di fusione della priorità per la traccia di animazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia.

</dd> <dt>

*Priorità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

Tenere traccia della priorità. Questo parametro deve essere impostato su una delle costanti di [**D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

---
description: Imposta le distanze minima e massima di intersezione tra oggetti 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: Metodo ID3DXPRTEngine::SetMinMaxIntersection (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2182714588e5d408c6928a677433e68dac44f09abf5ec6bd4cb4d6df7e4acf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629061"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>Metodo ID3DXPRTEngine::SetMinMaxIntersection

Imposta le distanze minima e massima di intersezione tra oggetti 3D. Questi valori di distanza possono essere usati per controllare la distanza minima o massima che gli oggetti possono nascondere o riflettere la luce. Ad esempio, il metodo può essere usato per limitare l'ombreggiatura delle caratteristiche vicine di un modello 3D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fMin* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distanza minima di intersezione. Deve essere positivo e minore di fMax.

</dd> <dt>

*fMax* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distanza massima di intersezione. Se 0,0f, verrà usato il valore precedente. in caso contrario, deve essere maggiore di fMin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo non può essere usato nelle simulazioni PRT (Precomputed Radiance Transfer) eseguite nella GPU. Vedere [**ID3DXPRTEngine::ComputeDirectLightingSHGPU.**](id3dxprtengine--computedirectlightingshgpu.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 

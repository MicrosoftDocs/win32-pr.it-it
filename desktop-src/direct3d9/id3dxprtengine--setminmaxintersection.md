---
description: Imposta le distanze minime e massime di intersezione tra oggetti 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Metodo ID3DXPRTEngine:: SetMinMaxIntersection (D3DX9Mesh. h)'
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
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355149"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>Metodo ID3DXPRTEngine:: SetMinMaxIntersection

Imposta le distanze minime e massime di intersezione tra oggetti 3D. Questi valori di distanza possono essere utilizzati per controllare la distanza minima o massima che gli oggetti possono nascondere o rispecchiare la luce. Ad esempio, il metodo può essere usato per limitare l'ombreggiatura delle funzionalità vicine di un modello 3D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fMin* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distanza di intersezione minima. Deve essere positivo e minore di fMax.

</dd> <dt>

*fMax* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distanza di intersezione massima. Se 0,0 f, verrà utilizzato il valore precedente; in caso contrario, deve essere maggiore di fMin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo non può essere usato nelle simulazioni dei PRT (pre-Computed Radiance Transfer) eseguite nella GPU. Vedere [**ID3DXPRTEngine:: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 

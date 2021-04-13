---
description: Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Metodo ID3DXRenderToEnvMap:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354564"
---
# <a name="id3dxrendertoenvmapend-method"></a>Metodo ID3DXRenderToEnvMap:: end

Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione valida di uno o più flag [di \_ filtro D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 

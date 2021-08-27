---
description: Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: Metodo ID3DXRenderToEnvMap::End (D3dx9core.h)
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
ms.openlocfilehash: efaf32eb421f6bda38fb922c4a89b1dbbe871842c3b4f07a87ff30c2e6b4dc40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095791"
---
# <a name="id3dxrendertoenvmapend-method"></a>Metodo ID3DXRenderToEnvMap::End

Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Filtro mip* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione valida di uno o più [flag \_ FILTER D3DX.](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 

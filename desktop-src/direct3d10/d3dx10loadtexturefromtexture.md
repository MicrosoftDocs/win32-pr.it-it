---
description: Caricare una trama da una trama.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Funzione D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354434"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>D3DX10LoadTextureFromTexture (funzione)

Caricare una trama da una trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntatore alla trama di origine. Vedere [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Tipo: **[ **d3dx10 \_ texture \_ Load \_ info**](d3dx10-texture-load-info.md)\***

Puntatore ai parametri di caricamento della trama. Vedere [**d3dx10 \_ texture \_ Load \_ info**](d3dx10-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntatore alla trama di destinazione. Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 





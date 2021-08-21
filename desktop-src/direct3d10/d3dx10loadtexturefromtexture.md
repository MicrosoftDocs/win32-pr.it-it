---
description: Caricare una trama da una trama.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Funzione D3DX10LoadTextureFromTexture (D3DX10Tex.h)
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
ms.openlocfilehash: bfc36423154bfd56f0695a3a8178b89aefce6e4dfc5a67f3866fa13a99c5e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990501"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>Funzione D3DX10LoadTextureFromTexture

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

Puntatore alla trama di origine. Vedere [**ID3D10Resource.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Tipo: **[ **D3DX10 \_ TEXTURE \_ LOAD \_ INFO**](d3dx10-texture-load-info.md)\***

Puntatore ai parametri di caricamento della trama. Vedere [**D3DX10 \_ TEXTURE LOAD \_ \_ INFO (INFORMAZIONI SUL CARICAMENTO TRAMA D3DX10).**](d3dx10-texture-load-info.md)

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntatore alla trama di destinazione. Vedere [**INTERFACCIA ID3D10Resource.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 





---
title: Funzione D3DX11LoadTextureFromTexture (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, ridimensionare, convertire, comprimere, decomprimere e/o CopyRectangle. Caricare una trama da una trama.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Funzione D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982322"
---
# <a name="d3dx11loadtexturefromtexture-function"></a>D3DX11LoadTextureFromTexture (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ridimensionare**, **convertire**, **comprimere**, **decomprimere** e/o **CopyRectangle**.

 

Caricare una trama da una trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* 
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Puntatore alla trama di origine. Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ texture \_ Load \_ info**](d3dx11-texture-load-info.md)\***

Puntatore ai parametri di caricamento della trama. Vedere [**D3DX11 \_ texture \_ Load \_ info**](d3dx11-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Puntatore alla trama di destinazione. Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 






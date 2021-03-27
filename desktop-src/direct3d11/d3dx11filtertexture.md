---
title: Funzione D3DX11FilterTexture (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GenerateMipMaps e GenerateMipMaps3D. Genera la catena mipmap usando un filtro di trama particolare.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Funzione D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982334"
---
# <a name="d3dx11filtertexture-function"></a>D3DX11FilterTexture (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** e **GenerateMipMaps3D**.

 

Genera la catena mipmap usando un filtro di trama particolare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pTexture* 
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Oggetto texture da filtrare. Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Livello mipmap i cui dati vengono usati per generare il resto della catena mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Flag che controllano il modo in cui ogni miplevel è filtrato (o D3DX11 \_ predefinito per il \_ filtro D3DX11 \_ lineare). Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).

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

 


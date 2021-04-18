---
description: Aggiunge uno sprite all'elenco di sprite in batch.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite: Metodo Raw:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323519"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite::D Metodo Raw

Aggiunge uno sprite all'elenco di sprite in batch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama sprite.

</dd> <dt>

*pSrcRect* \[ in\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che indica la parte della trama di origine da usare per lo sprite. Se questo parametro è **null**, viene usata l'intera immagine di origine per lo sprite.

</dd> <dt>

*pCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che identifica il centro dello sprite. Se questo argomento è **null**, viene utilizzato il punto (0, 0, 0), ovvero l'angolo superiore sinistro.

</dd> <dt>

*pPosition* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che identifica la posizione dello sprite. Se questo argomento è **null**, viene utilizzato il punto (0, 0, 0), ovvero l'angolo superiore sinistro.

</dd> <dt>

*Colore* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Tipo [**D3DCOLOR**](d3dcolor.md) . Il colore e i canali alfa vengono modulati in base a questo valore. Il valore 0xFFFFFFFF mantiene il colore di origine e i dati alfa originali. Usare la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) per generare questo colore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Per ridimensionare, ruotare o tradurre uno sprite, chiamare [**ID3DXSprite:: setransform**](id3dxsprite--settransform.md) con una matrice che contiene i valori scale, Rotate e translate (SRT), prima di chiamare ID3DXSprite::D RAW. Per informazioni sull'impostazione di valori SRT in una matrice, vedere [trasformazioni matrici](transforms.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 

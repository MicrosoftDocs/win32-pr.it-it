---
description: Disegnare una matrice di sprite.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: Metodo ID3DX10Sprite::D rawSpritesImmediate (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0a3295d64efc3f3ff05b39e0866a15fb7eed9ba2d8c580fe2c7b219d36708e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046899"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>Metodo ID3DX10Sprite::D rawSpritesImmediate

Disegnare una matrice di sprite. Gli sprite verranno inviati immediatamente al dispositivo per il rendering, che è diverso da [**ID3DX10Sprite::D rawSpritesBuffered,**](id3dx10sprite-drawspritesbuffered.md) che aggiunge solo una matrice di sprite a un batch di sprite di cui eseguire il rendering quando viene chiamato [**ID3DX10Sprite::Flush.**](id3dx10sprite-flush.md) Questo metodo di disegno è particolarmente utile quando si disegna un numero elevato di sprite che sono già stati ordinati nella CPU (o non devono essere ordinati), ad esempio in un sistema di particelle. Deve essere chiamato tra le chiamate a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End.**](id3dx10sprite-end.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSprites* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***

Matrice di sprite da disegnare. Vedere [**D3DX10 \_ SPRITE.**](d3dx10-sprite.md)

</dd> <dt>

*cSprites* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di sprite in pSprites.

</dd> <dt>

*cbSprite* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensione della struttura sprite che si sta passando in pSprites. Il passaggio di 0 equivale a passare sizeof(D3DX10 \_ SPRITE).

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

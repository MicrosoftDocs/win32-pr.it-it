---
description: Creare una matrice di sprite.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: Metodo ID3DX10Sprite::D rawSpritesImmediate (D3DX10. h)
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
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356119"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite::D Metodo rawSpritesImmediate

Creare una matrice di sprite. Questa operazione invierà immediatamente gli sprite al dispositivo per il rendering, che è diverso da [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) che aggiunge una matrice di sprite a un batch di sprite di cui eseguire il rendering quando viene chiamato [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) . Questo metodo di disegno è particolarmente utile quando si disegna un numero elevato di sprite che sono già stati ordinati sulla CPU (o che non devono essere ordinati), ad esempio in un sistema particellare. Questo deve essere chiamato tra le chiamate a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).

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

*pSprites* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ sprite**](d3dx10-sprite.md)\***

Matrice di sprite da creare. Vedere [**d3dx10 \_ sprite**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di sprite in pSprites.

</dd> <dt>

*cbSprite* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensione della struttura sprite che si passa a pSprites. Il passaggio di 0 equivale al passaggio di sizeof (D3DX10 \_ sprite).

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

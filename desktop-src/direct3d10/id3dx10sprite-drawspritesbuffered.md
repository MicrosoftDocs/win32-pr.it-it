---
description: Aggiungere una matrice di sprite al batch di sprite di cui eseguire il rendering.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: Metodo ID3DX10Sprite::D rawSpritesBuffered (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323746"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite::D Metodo rawSpritesBuffered

Aggiungere una matrice di sprite al batch di sprite di cui eseguire il rendering. Questo deve essere chiamato tra le chiamate a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: end**](id3dx10sprite-end.md)e [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) deve essere chiamato prima di end per inviare tutti gli sprite in batch al dispositivo per il rendering. Questo metodo di disegno è particolarmente utile quando si disegna un numero ridotto di sprite che si desidera memorizzare nel buffer in un batch di grandi dimensioni, ad esempio i tipi di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

 

 

---
description: Creare uno sprite per disegnare una trama 2D. Nota Invece di usare questa funzione, è consigliabile usare Direct2D e la libreria DirectXTK, la classe SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Funzione D3DX10CreateSprite (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f67a0a6e0be8a3ea71ff1eef46d72b6cf080d028e7cc32f72a52db6a209cea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541061"
---
# <a name="d3dx10createsprite-function"></a>Funzione D3DX10CreateSprite

Creare uno sprite per disegnare una trama 2D.

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare [Direct2D](../direct2d/direct2d-portal.md) e la libreria [DirectXTK,](https://github.com/Microsoft/DirectXTK) **la classe SpriteBatch.**

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo (vedere [**ID3D10 InterfaceDevice Interface)**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)che disegna lo sprite.

</dd> <dt>

*cDeviceBufferSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensioni del buffer dei vertici, in numero di sprite, che verranno inviate al dispositivo quando viene chiamato [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawSpritesImmediate.**](id3dx10sprite-drawspritesimmediate.md) Dovrebbe trattarsi di un numero ridotto se si è in grado di eseguire il rendering di un numero ridotto di sprite alla volta (per risparmiare memoria) e di un numero elevato se si è in grado di eseguire il rendering di un numero elevato di sprite alla volta. Il valore massimo è 4096. Se viene specificato 0, la dimensione del buffer dei vertici verrà impostata automaticamente su 4096.

</dd> <dt>

*ppSprite* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Indirizzo di un puntatore a un'interfaccia sprite (vedere [**l'interfaccia ID3DX10Sprite).**](id3dx10sprite.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

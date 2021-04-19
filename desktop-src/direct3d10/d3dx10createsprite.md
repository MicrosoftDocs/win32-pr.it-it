---
description: Creare uno sprite per il disegno di una trama 2D. Nota invece di utilizzare questa funzione, è consigliabile utilizzare Direct2D e la libreria DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Funzione D3DX10CreateSprite (D3DX10. h)
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
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322414"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite (funzione)

Creare uno sprite per il disegno di una trama 2D.

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare [Direct2D](../direct2d/direct2d-portal.md) e la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.

 

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che trarrà lo sprite.

</dd> <dt>

*cDeviceBufferSize* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensioni del buffer dei vertici, in numero di sprite, che verranno inviate al dispositivo quando viene chiamato [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) . Si tratta di un numero ridotto se si è certi che verrà eseguito il rendering di un numero ridotto di sprite alla volta (per risparmiare memoria) e un numero elevato se si è certi che verrà eseguito il rendering di un numero elevato di sprite alla volta. Il valore massimo è 4096. Se si specifica 0, le dimensioni del buffer vertici verranno impostate automaticamente su 4096.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Indirizzo di un puntatore a un'interfaccia sprite (vedere [**interfaccia ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

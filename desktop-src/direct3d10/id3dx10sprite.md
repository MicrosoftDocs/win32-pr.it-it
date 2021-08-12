---
description: L'interfaccia ID3DX10Sprite fornisce un set di metodi che semplificano il processo di disegno di sprite con Microsoft Direct3D. Questa interfaccia può operare su un set di molti sprite.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: Interfaccia ID3DX10Sprite (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301929"
---
# <a name="id3dx10sprite-interface"></a>Interfaccia ID3DX10Sprite

L'interfaccia ID3DX10Sprite fornisce un set di metodi che semplificano il processo di disegno di sprite con Microsoft Direct3D. Questa interfaccia può operare su un set di molti sprite.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10Sprite** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Sprite** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10Sprite** include questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inizia**](id3dx10sprite-begin.md)                                   | Preparare un dispositivo per il disegno di sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Aggiungere una matrice di sprite al batch di sprite di cui eseguire il rendering. Questo deve essere chiamato tra le chiamate a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End**](id3dx10sprite-end.md)e [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) deve essere chiamato prima di End per inviare tutti gli sprite in batch al dispositivo per il rendering. Questo metodo di disegno è particolarmente utile quando si disegna un numero ridotto di sprite che si vuole inserire nel buffer in un batch di grandi dimensioni, ad esempio i tipi di carattere.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Disegnare una matrice di sprite. Gli sprite verranno inviati immediatamente al dispositivo per il rendering, che è diverso da [**ID3DX10Sprite::D rawSpritesBuffered,**](id3dx10sprite-drawspritesbuffered.md) che aggiunge solo una matrice di sprite a un batch di sprite di cui eseguire il rendering quando viene chiamato [**ID3DX10Sprite::Flush.**](id3dx10sprite-flush.md) Questo metodo di disegno è particolarmente utile quando si disegna un numero elevato di sprite che sono già stati ordinati nella CPU (o non devono essere ordinati), ad esempio in un sistema di particelle. Deve essere chiamato tra le chiamate a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End.**](id3dx10sprite-end.md)<br/> |
| [**Fine**](id3dx10sprite-end.md)                                       | Chiamare questo metodo dopo ID3DX10Sprite::Flush. Se al momento della chiamata a ID3DX10Sprite::Begin è stato specificato D3DX10 SPRITE SAVE STATE, questa API ripristina lo stato del dispositivo allo stato precedente alla chiamata di \_ \_ \_ ID3DX10Sprite::Begin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Svuotamento**](id3dx10sprite-flush.md)                                   | Forzare l'invio di tutti gli sprite in batch al dispositivo. Gli stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DX10Sprite::Begin. L'elenco degli sprite in batch viene quindi cancellato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Recuperare il dispositivo associato all'oggetto sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Ottiene la matrice di proiezione dello sprite applicata a tutti gli sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Ottiene la trasformazione di visualizzazione che si applica a tutti gli sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Impostare la matrice di proiezione per tutti gli sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Impostare la trasformazione di visualizzazione che si applica a tutti gli sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DX10Sprite viene ottenuta chiamando la [**funzione D3DX10CreateSprite.**](d3dx10createsprite.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

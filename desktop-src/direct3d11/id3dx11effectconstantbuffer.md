---
title: Interfaccia ID3DX11EffectConstantBuffer (D3dx11effect.h)
description: Un'interfaccia constant-buffer accede a buffer costanti o buffer di trama.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c5e62e6d339482123f66b7f23aae771f335392b54b9a766681dab78f6fbafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851641"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Interfaccia ID3DX11EffectConstantBuffer

Un'interfaccia constant-buffer accede a buffer costanti o buffer di trama.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectConstantBuffer** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectConstantBuffer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectConstantBuffer** include questi metodi.



| Metodo                                                                             | Descrizione                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Ottiene un constant-buffer.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Ottiene un buffer di trama.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Impostare un constant-buffer.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Impostare un buffer di trama.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Ripristina un buffer costante impostato in precedenza.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Ripristina un buffer di trama impostato in precedenza.<br/>  |



 

## <a name="remarks"></a>Commenti

Usare i buffer costanti per archiviare molte costanti di effetto. raggruppamento di costanti in buffer in base alla frequenza di aggiornamento. In questo modo è possibile ridurre al minimo il numero di modifiche di stato e effettuare il numero più ridotto di chiamate API per modificare lo stato. Entrambi questi fattori determinano prestazioni migliori.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce effetti 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






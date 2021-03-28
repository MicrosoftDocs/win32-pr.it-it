---
title: Interfaccia ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Un'interfaccia con buffer costante accede a buffer costanti o a buffer di trama.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, descritta
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
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355254"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Interfaccia ID3DX11EffectConstantBuffer

Un'interfaccia con buffer costante accede a buffer costanti o a buffer di trama.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectConstantBuffer** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectConstantBuffer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectConstantBuffer** dispone di questi metodi.



| Metodo                                                                             | Descrizione                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Ottenere un buffer costante.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Ottenere un buffer di trama.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Impostare un buffer di costanti.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Impostare un buffer di trama.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Ripristina un buffer costante impostato in precedenza.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Ripristina un buffer di trama impostato in precedenza.<br/>  |



 

## <a name="remarks"></a>Commenti

Usare i buffer costanti per archiviare molte costanti di effetto; raggruppamento di costanti in buffer in base alla relativa frequenza di aggiornamento. Questo consente di ridurre al minimo il numero di modifiche allo stato e di effettuare il minor numero di chiamate API per modificare lo stato. Entrambi questi fattori consentono di ottenere prestazioni migliori.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






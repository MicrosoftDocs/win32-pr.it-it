---
description: L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interfaccia ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235038"
---
# <a name="id3dx10font-interface"></a>Interfaccia ID3DX10Font

L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10Font** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Font** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10Font** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dx10font-drawtext.md)                   | Creare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Restituisce un handle a un contesto di periferica di visualizzazione (DC) sul quale è impostato il tipo di carattere.<br/>                                                            |
| [**Getdesc**](id3dx10font-getdesc.md)                     | Ottiene una descrizione dell'oggetto del tipo di carattere corrente.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Recuperare le caratteristiche dei tipi di carattere.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Caricare una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DX10Font viene ottenuta chiamando [**D3DX10CreateFont**](d3dx10createfont.md) o [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).

Il tipo LPD3DX10FONT è definito come puntatore all'interfaccia ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

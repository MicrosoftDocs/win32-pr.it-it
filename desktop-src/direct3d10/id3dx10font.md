---
description: L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interfaccia ID3DX10Font (D3DX10.h)
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
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540347"
---
# <a name="id3dx10font-interface"></a>Interfaccia ID3DX10Font

L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10Font** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Font** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10Font** include questi metodi.



| Metodo                                                     | Descrizione                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dx10font-drawtext.md)                   | Disegnare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Restituisce un handle a un contesto di dispositivo di visualizzazione (DC) in cui è impostato il tipo di carattere.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Ottiene una descrizione dell'oggetto tipo di carattere corrente.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.<br/>                                                     |
| [**GetTextMetrics**](id3dx10font-gettextmetrics.md)       | Recupera le caratteristiche del carattere.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Caricare una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                        |
| [**PreloadGlyphs**](id3dx10font-preloadglyphs.md)         | Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Caricare testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DX10Font viene ottenuta chiamando [**D3DX10CreateFont**](d3dx10createfont.md) o [**D3DX10CreateFontIndirect.**](d3dx10createfontindirect.md)

Il tipo LPD3DX10FONT è definito come puntatore all'interfaccia ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

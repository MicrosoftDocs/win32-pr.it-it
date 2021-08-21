---
description: L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interfaccia ID3DXFont (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f05322ef2d7898f0025154989e9ac09ab8355025d8ad1ed94034fb25da66592f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493652"
---
# <a name="id3dxfont-interface"></a>Interfaccia ID3DXFont

L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.

## <a name="members"></a>Membri

**L'interfaccia ID3DXFont** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFont** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXFont** include questi metodi.



| Metodo                                                    | Descrizione                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dxfont--drawtext.md)                   | Disegna testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Restituisce un handle per un contesto di dispositivo di visualizzazione (DC) con il tipo di carattere impostato.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Ottiene una descrizione dell'oggetto tipo di carattere corrente. GetDescW e GetDescA sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito rispettivamente a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ DESCA.**<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Recupera il dispositivo Direct3D associato all'oggetto tipo di carattere.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Recupera le caratteristiche del carattere identificate in una [**struttura TEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ID3DXFont** viene ottenuta chiamando [**D3DXCreateFont**](d3dxcreatefont.md) o [**D3DXCreateFontIndirect.**](d3dxcreatefontindirect.md)

Il tipo LPD3DXFONT è definito come puntatore **all'interfaccia ID3DXFont.**


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

---
description: L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interfaccia ID3DXFont (D3dx9core. h)
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
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323538"
---
# <a name="id3dxfont-interface"></a>Interfaccia ID3DXFont

L'interfaccia ID3DXFont incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.

## <a name="members"></a>Membri

L'interfaccia **ID3DXFont** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFont** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXFont** dispone di questi metodi.



| Metodo                                                    | Descrizione                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dxfont--drawtext.md)                   | Disegna il testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Restituisce un handle per un contesto di periferica di visualizzazione (DC) con il set di caratteri.<br/>                                                                                                                                                           |
| [**Getdesc**](id3dxfont--getdesc.md)                     | Ottiene una descrizione dell'oggetto del tipo di carattere corrente. GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , rispettivamente.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Recupera il dispositivo Direct3D associato all'oggetto del tipo di carattere.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Recupera le caratteristiche dei tipi di carattere identificate in una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

L'interfaccia **ID3DXFont** viene ottenuta chiamando [**D3DXCreateFont**](d3dxcreatefont.md) o [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).

Il tipo LPD3DXFONT è definito come puntatore all'interfaccia **ID3DXFont** .


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

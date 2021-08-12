---
description: Disegnare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: Metodo ID3DX10Font::D rawText (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303171"
---
# <a name="id3dx10fontdrawtext-method"></a>Metodo ID3DX10Font::D rawText

Disegnare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSprite* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Puntatore a un oggetto ID3DX10Sprite contenente la stringa da disegnare. Può essere **NULL,** nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto sprite. Per migliorare l'efficienza, è necessario specificato un oggetto sprite se ID3DX10Font::D rawText deve essere chiamato più volte in una riga.

</dd> <dt>

*pString* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa da disegnare. Se viene definito UNICODE, questo tipo di parametro viene risolto in un LPCWSTR. In caso contrario, il tipo viene risolto in un LPCSTR. Se il parametro Count è -1, la stringa deve terminare **con NULL.**

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Numero di caratteri nella stringa. Se Count è -1, si presuppone che il parametro pString sia un puntatore a uno sprite contenente una stringa con terminazione NULL e ID3DX10Font::D rawText calcola automaticamente il numero di caratteri.

</dd> <dt>

*pRect* \[ Pollici\]
</dt> <dd>

Tipo: **LPRECT**

Puntatore a [una struttura RECT](/previous-versions//ms536136(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo. Come per qualsiasi oggetto RECT, il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro. Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Specificare il metodo di formattazione del testo. Può essere qualsiasi combinazione dei valori seguenti:



| Elemento                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ BOTTOM<br/>             | Giustificare il testo alla fine del rettangolo. Questo valore deve essere combinato con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Indicare a DrawText di calcolare automaticamente la larghezza e l'altezza del rettangolo in base alla lunghezza della stringa da disegnare. Se sono presenti più righe di testo, ID3DX10Font::D rawText usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per delimitare l'ultima riga di testo. Se è presente una sola riga di testo, ID3DX10Font::D rawText modifica il lato destro del rettangolo in modo da delimitare l'ultimo carattere nella riga. In entrambi i casi, ID3DX10Font::D rawText restituisce l'altezza del testo formattato, ma non disegna il testo.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>CENTRO \_ DT<br/>             | Centrare il testo orizzontalmente nel rettangolo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | Espandere i caratteri di tabulazione. Il numero predefinito di caratteri per tabulazione è otto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ LEFT<br/>                   | Allineare il testo a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOCLIP<br/>             | Disegnare senza ritaglio. ID3DX10Font::D rawText è leggermente più veloce quando si usa DT \_ NOCLIP.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ RIGHT<br/>                | Allineare il testo a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Visualizzare il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando è selezionato un tipo di carattere ebraico o arabo. L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE<br/> | Visualizzare il testo solo su una singola riga. I ritorni a capo e gli avanzamento riga non interrompno la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP<br/>                      | Testo giustificato in alto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER<br/>          | Centrare il testo verticalmente (solo riga singola).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | Parole di interruzione. Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect. Anche una sequenza di ritorno a capo/avanzamento riga interrompe la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Colore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore del testo. Vedere [**D3DXCOLOR.**](d3d10-d3dxcolor.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche. Se viene specificato DT VCENTER o DT BOTTOM, il valore restituito è l'offset da \_ \_ pRect (dall'alto verso il basso) del testo disegnato. Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I parametri di questo metodo sono molto simili a quelli della [funzione DrawText GDI.](/previous-versions//ms533909(v=vs.85))

Questo metodo supporta sia stringhe ANSI che Unicode.

A meno che non venga usato il formato DT NOCLIP, questo metodo ritaglia il testo in modo che non venga \_ visualizzato all'esterno del rettangolo specificato. Si presuppone che tutta la formattazione abbia più righe, a meno che non venga specificato il formato \_ SINGLELINE DT.

Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.

Questo metodo supporta solo i tipi di carattere i cui caratteri di escape e orientamento sono entrambi pari a zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

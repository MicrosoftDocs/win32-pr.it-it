---
description: Creare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: Metodo ID3DX10Font::D rawText (D3DX10. h)
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
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322762"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font::D Metodo rawText

Creare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.

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

*pSprite* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Puntatore a un oggetto ID3DX10Sprite che contiene la stringa che si vuole creare. Può essere **null**, nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto Sprite. Per migliorare l'efficienza, è necessario specificare un oggetto Sprite se ID3DX10Font::D rawText deve essere chiamato più di una volta in una riga.

</dd> <dt>

*pString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa da creare. Se è definito UNICODE, questo tipo di parametro viene risolto in un LPCWSTR; in caso contrario, il tipo viene risolto in un LPCSTR. Se il parametro count è-1, la stringa deve essere con terminazione **null** .

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Numero di caratteri nella stringa. Se count è-1, viene utilizzato il parametro pString come puntatore a uno sprite contenente una stringa con terminazione NULL e ID3DX10Font::D rawText calcola automaticamente il numero di caratteri.

</dd> <dt>

*pRect* \[ in\]
</dt> <dd>

Tipo: **lpRect**

Puntatore a una struttura [Rect](/previous-versions//ms536136(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo. Come per qualsiasi oggetto RECT, il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro. Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Specificare il metodo di formattazione del testo. Può essere una qualsiasi combinazione dei valori seguenti:



| Elemento                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ inferiore<br/>             | Giustifica il testo nella parte inferiore del rettangolo. Questo valore deve essere combinato con DT \_ Singleline.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Indicare a DrawText di calcolare automaticamente la larghezza e l'altezza del rettangolo in base alla lunghezza della stringa che si indica di creare. Se sono presenti più righe di testo, ID3DX10Font::D rawText usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per l'associazione dell'ultima riga di testo. Se è presente una sola riga di testo, ID3DX10Font::D rawText modifica il lato destro del rettangolo in modo da delegare l'ultimo carattere nella riga. In entrambi i casi, ID3DX10Font::D rawText restituisce l'altezza del testo formattato ma il testo non viene disegnato.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>centro di DT \_<br/>             | Centra il testo orizzontalmente nel rettangolo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ ExpandTabs<br/> | Espandere i caratteri di tabulazione. Il numero predefinito di caratteri per tabulazione è otto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT a \_ sinistra<br/>                   | Allinea il testo a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip<br/>             | Viene disegnato senza ritaglio. ID3DX10Font::D rawText è leggermente più veloce quando \_ si usa DT noclip.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT a \_ destra<br/>                | Allinea il testo a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Consente di visualizzare il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando viene selezionato un tipo di carattere ebraico o arabo. L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ Singleline<br/> | Visualizza il testo solo su una sola riga. I ritorni a capo e i feed di riga non interrompono la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ superiore<br/>                      | Testo in primo piano.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_vCenter vCenter<br/>          | Centra il testo verticalmente (solo riga singola).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WordBreak<br/>    | Interrompi parole. Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect. Una sequenza di ritorno A capo/avanzamento riga interrompe anche la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Colore* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore del testo. Vedere [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo nelle unità logiche. Se \_ si specifica DT vCenter o DT \_ Bottom, il valore restituito è l'offset da pRect (dall'alto verso il basso) del testo creato. Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I parametri di questo metodo sono molto simili a quelli della funzione [DrawText di GDI](/previous-versions//ms533909(v=vs.85)) .

Questo metodo supporta le stringhe ANSI e Unicode.

A meno che non \_ venga utilizzato il formato DT noclip, questo metodo consente di ritagliare il testo in modo che non venga visualizzato all'esterno del rettangolo specificato. Si presuppone che tutte le formattazioni abbiano più righe, a meno che non \_ sia specificato il formato DT Singleline.

Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.

Questo metodo supporta solo i tipi di carattere il cui scappamento e l'orientamento sono entrambi zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

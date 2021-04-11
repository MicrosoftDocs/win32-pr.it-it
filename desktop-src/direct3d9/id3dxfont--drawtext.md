---
description: Disegna il testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: Metodo ID3DXFont::D rawText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235010"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont::D Metodo rawText

Disegna il testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSprite* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Puntatore a un oggetto [**ID3DXSprite**](id3dxsprite.md) che contiene la stringa. Può essere **null**, nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto Sprite. Per migliorare l'efficienza, è necessario specificare un oggetto Sprite se **DrawText** viene chiamato più di una volta in una riga.

</dd> <dt>

*pString* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa da creare. Se il parametro count è-1, la stringa deve essere con terminazione null.

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Specifica il numero di caratteri nella stringa. Se count è-1, il parametro pString viene considerato un puntatore a una stringa con terminazione null e **DrawText** calcola automaticamente il numero di caratteri.

</dd> <dt>

*pRect* \[ in\]
</dt> <dd>

Tipo: **[ **lpRect**](../winprog/windows-data-types.md)**

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo. Il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro. Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il metodo di formattazione del testo. Può essere una qualsiasi combinazione dei valori seguenti:



| Valore                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ inferiore**</dt> </dl>             | Giustifica il testo nella parte inferiore del rettangolo. Questo valore deve essere combinato con DT \_ Singleline.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | Determina la larghezza e l'altezza del rettangolo. Se sono presenti più righe di testo, **DrawText** usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per l'associazione dell'ultima riga di testo. Se è presente una sola riga di testo, **DrawText** modifica il lato destro del rettangolo in modo da delegare l'ultimo carattere nella riga. In entrambi i casi, per **DrawText** viene restituita l'altezza del testo formattato ma il testo non viene disegnato.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**centro di DT \_**</dt> </dl>             | Centra il testo orizzontalmente nel rettangolo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ ExpandTabs**</dt> </dl> | Espande i caratteri di tabulazione. Il numero predefinito di caratteri per tabulazione è otto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT a \_ sinistra**</dt> </dl>                   | Allinea il testo a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOclip**</dt> </dl>             | Disegna senza ritaglio. **DrawText** è leggermente più veloce quando \_ si usa DT noclip.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT a \_ destra**</dt> </dl>                | Allinea il testo a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | Visualizza il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando viene selezionato un tipo di carattere ebraico o arabo. L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ Singleline**</dt> </dl> | Visualizza il testo solo su una sola riga. I ritorni a capo e i feed di riga non interrompono la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ superiore**</dt> </dl>                      | Top: giustifica il testo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**\_vCenter vCenter**</dt> </dl>          | Centra il testo verticalmente (solo riga singola).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WordBreak**</dt> </dl>    | Interrompe le parole. Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect. Una sequenza di ritorno A capo/avanzamento riga interrompe anche la riga.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Colore* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Colore del testo. Per ulteriori informazioni, vedere [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo nelle unità logiche. Se \_ si specifica DT vCenter o DT \_ Bottom, il valore restituito è l'offset da pRect (dall'alto verso il basso) del testo creato. Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I parametri di questo metodo sono molto simili a quelli della funzione [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) di GDI.

Questo metodo supporta le stringhe ANSI e Unicode.

Questo metodo deve essere chiamato all'interno di un [**BeginScene**](/windows/desktop/api) ... Blocco [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) . L'unica eccezione è rappresentata dal caso in cui un'applicazione chiama **DrawText** con DT \_ CALCRECT per calcolare le dimensioni di un blocco di testo specificato.

A meno che non \_ venga utilizzato il formato DT noclip, questo metodo consente di ritagliare il testo in modo che non venga visualizzato all'esterno del rettangolo specificato. Si presuppone che tutte le formattazioni abbiano più righe, a meno che non \_ sia specificato il formato DT Singleline.

Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.

Questo metodo supporta solo i tipi di carattere il cui scappamento e l'orientamento sono entrambi zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 

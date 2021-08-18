---
description: Disegna testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: Metodo ID3DXFont::D rawText (D3dx9core.h)
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
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987421"
---
# <a name="id3dxfontdrawtext-method"></a>Metodo ID3DXFont::D rawText

Disegna testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.

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

*pSprite* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Puntatore a [**un oggetto ID3DXSprite**](id3dxsprite.md) che contiene la stringa. Può essere **NULL,** nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto sprite. Per migliorare l'efficienza, è necessario specificato un oggetto sprite se **DrawText** deve essere chiamato più volte in una riga.

</dd> <dt>

*pString* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa da disegnare. Se il parametro Count è -1, la stringa deve essere con terminazione Null.

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Specifica il numero di caratteri nella stringa. Se Count è -1, si presuppone che il parametro pString sia un puntatore a una stringa con terminazione Null e **DrawText** calcola automaticamente il numero di caratteri.

</dd> <dt>

*pRect* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPRECT**](../winprog/windows-data-types.md)**

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo. Il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro. Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il metodo di formattazione del testo. Può essere qualsiasi combinazione dei valori seguenti:



| Valore                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ BOTTOM**</dt> </dl>             | Giustifica il testo nella parte inferiore del rettangolo. Questo valore deve essere combinato con DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | Determina la larghezza e l'altezza del rettangolo. Se sono presenti più righe di testo, **DrawText** usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per delimitare l'ultima riga di testo. Se è presente una sola riga di testo, **DrawText** modifica il lato destro del rettangolo in modo che limiti l'ultimo carattere nella riga. In entrambi i **casi, DrawText** restituisce l'altezza del testo formattato, ma non disegna il testo.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**CENTRO \_ DT**</dt> </dl>             | Centra il testo orizzontalmente nel rettangolo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ EXPANDTABS**</dt> </dl> | Espande i caratteri di tabulazione. Il numero predefinito di caratteri per tabulazione è otto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT \_ LEFT**</dt> </dl>                   | Allinea il testo a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOCLIP**</dt> </dl>             | Disegna senza ritaglio. **DrawText** è un po' più veloce quando si usa DT \_ NOCLIP.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT \_ RIGHT**</dt> </dl>                | Allinea il testo a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | Visualizza il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando è selezionato un tipo di carattere ebraico o arabo. L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ SINGLELINE**</dt> </dl> | Visualizza il testo solo su una singola riga. I ritorni a capo e gli avanzamento riga non interrompeno la riga.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ TOP**</dt> </dl>                      | Testo giustificato in primo piano.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**DT \_ VCENTER**</dt> </dl>          | Centra il testo verticalmente (solo riga singola).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WORDBREAK**</dt> </dl>    | Interrompe le parole. Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect. Anche una sequenza di ritorno a capo/avanzamento riga interrompe la riga.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Colore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Colore del testo. Per altre informazioni, vedere [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche. Se si specificato DT VCENTER o DT BOTTOM, il valore restituito è l'offset da \_ \_ pRect (dall'alto verso il basso) del testo disegnato. Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I parametri di questo metodo sono molto simili a quelli della funzione [**GDI DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext)

Questo metodo supporta sia stringhe ANSI che Unicode.

Questo metodo deve essere chiamato all'interno di [**un oggetto BeginScene**](/windows/desktop/api) ... [**Blocco EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) L'unica eccezione si verifica quando un'applicazione chiama **DrawText** con DT CALCRECT per calcolare le dimensioni di \_ un determinato blocco di testo.

A meno che non venga usato il formato NOCLIP DT, questo metodo ritaglia il testo in modo che non venga \_ visualizzato all'esterno del rettangolo specificato. Si presuppone che tutta la formattazione abbia più righe, a meno che non venga specificato il formato \_ DT SINGLELINE.

Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.

Questo metodo supporta solo tipi di carattere il cui carattere di escape e orientamento sono entrambi pari a zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 

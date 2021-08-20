---
title: SB_SETTEXT messaggio (Commctrl.h)
description: Imposta il testo nella parte specificata di una finestra di stato.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fcf0a7928e87cbc614a59dc64b433223afa97bbdac3f45f1635cb8cfe7b34a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408884"
---
# <a name="sb_settext-message"></a>Messaggio \_ SETTEXT SB

Imposta il testo nella parte specificata di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) della parola meno importante specifica l'indice in base zero della parte da impostare. Se **l'opzione LOBYTE** è impostata su SB SIMPLEID, si presuppone che la finestra di stato sia una barra di stato in modalità semplice, ad esempio una barra di stato con \_ una sola parte.

[**L'HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) della parola meno ordinata specifica il tipo di operazione di disegno. Questo parametro può avere uno dei valori seguenti.

La parola di ordine superiore *di wParam viene* ignorata.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td>Il testo viene disegnato con un bordo inferiore al piano della finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>Il testo viene disegnato senza bordi.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>Il testo viene disegnato dalla finestra padre. <br/>
<blockquote>
[!Note]<br />
Una barra di stato in modalità semplice non supporta il disegno da parte del proprietario.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>Il testo viene disegnato con un bordo superiore al piano della finestra.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>Il testo verrà visualizzato nella direzione opposta al testo nella finestra padre.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>I caratteri di tabulazione vengono ignorati.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il testo da impostare. Se *wParam* è SBT \_ OWNERDRAW, questo parametro rappresenta 32 bit di dati. La finestra padre deve interpretare i dati e disegnare il testo quando riceve il [**messaggio WM \_ DRAWITEM.**](wm-drawitem.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il messaggio invalida la parte della finestra che è stata modificata, causando la visualizzazione del nuovo testo alla successiva ricezione del messaggio [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) da parte della finestra.

Le finestre normali visualizzano il testo da sinistra a destra. Windows possibile eseguire *il mirroring per* visualizzare lingue come l'ebraico o l'arabo che leggono da destra a sinistra (RTL). Se la proprietà SBT RTLREADING è impostata, la stringa lParam verrà letta nella direzione opposta rispetto al testo \_ nella finestra padre. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) e **SB \_ SETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SB \_ GETTEXT**](sb-gettext.md)
</dt> </dl>

 


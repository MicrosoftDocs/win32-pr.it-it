---
title: Messaggio SB_SETTEXT (COMmctrl. h)
description: Imposta il testo nella parte specificata di una finestra di stato.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Controlli di Windows Message SB_SETTEXT
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
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120695"
---
# <a name="sb_settext-message"></a>\_Messaggio di testo SB

Imposta il testo nella parte specificata di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) della parola di ordine inferiore specifica l'indice in base zero della parte da impostare. Se **LOBYTE** è impostato su SB \_ SIMPLEID, si presuppone che la finestra di stato sia una barra di stato in modalità semplice, ovvero una barra di stato con una sola parte.

Il [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) della parola di ordine inferiore specifica il tipo di operazione di disegno. Questo parametro può avere uno dei valori seguenti.

La parola più ordinata di *wParam* viene ignorata.



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
<td>Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.<br/></td>
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
Una barra di stato in modalità semplice non supporta il disegno del proprietario.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.<br/></td>
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

Puntatore a una stringa con terminazione null che specifica il testo da impostare. Se *wParam* è SBT \_ OWNERDRAW, questo parametro rappresenta 32 bit di dati. La finestra padre deve interpretare i dati e creare il testo quando riceve il messaggio [**WM \_ DrawItem**](wm-drawitem.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il messaggio invalida la parte della finestra che è stata modificata, causando la visualizzazione del nuovo testo quando la finestra successiva riceve il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .

Normale testo visualizzato da sinistra a destra (LTR). È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL). Se \_ si imposta SBT RTLREADING, la stringa *lParam* verrà letta nella direzione opposta dal testo nella finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) e **SB \_ setexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SB \_ GETtext**](sb-gettext.md)
</dt> </dl>

 


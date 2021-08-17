---
title: SB_GETTEXT messaggio (Commctrl.h)
description: Recupera il testo dalla parte specificata di una finestra di stato.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05967d41d86ad039e39259c8179a9e768e8fbbf76e5112b531048ac0ed7b56bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168729"
---
# <a name="sb_gettext-message"></a>Messaggio \_ GETTEXT SB

Recupera il testo dalla parte specificata di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte da cui recuperare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve il testo come stringa con terminazione Null. Usare il [**messaggio SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per determinare le dimensioni richieste del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit costituito da due valori a 16 bit. La parola bassa specifica la lunghezza, in caratteri, del testo. La parola alta specifica il tipo di operazione usata per disegnare il testo. Il tipo può essere uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Il testo viene disegnato con un bordo inferiore al piano della finestra.<br/>  |
| <dl> <dt>**\_NOBORDER SBT**</dt> </dl>  | Il testo viene disegnato senza bordi.<br/>                                             |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | Il testo viene disegnato con un bordo che viene visualizzato più in alto rispetto al piano della finestra.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Il testo viene visualizzato nella direzione opposta del testo nella finestra padre.<br/>  |



 

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso non corretto di questo messaggio può compromettere la sicurezza del programma. Questo messaggio non consente di conoscere le dimensioni del buffer. Se si usa questo messaggio, chiamare [**prima SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere il numero di caratteri necessari e quindi chiamare il messaggio per recuperare la stringa. Se si attende prima di chiamare **SB \_ GETTEXT,** il testo potrebbe cambiare, invalidando così il valore restituito **di SB \_ GETTEXTLENGTH**. Prima di continuare, vedere Considerazioni sulla [sicurezza: Microsoft Windows Controlli.](sec-comctls.md)

Questo messaggio restituisce un massimo di 65.535 caratteri. Se la stringa di testo è più lunga, viene troncata.

Se il testo ha il tipo di disegno SBT OWNERDRAW, questo messaggio restituisce il valore a 32 bit associato al testo anziché la lunghezza e il tipo \_ di operazione.

Le finestre normali visualizzano il testo da sinistra a destra (LTR). Windows può essere *speculare* per visualizzare lingue come l'ebraico o l'arabo che leggono da destra a sinistra (RTL). Se la proprietà SBT RTLREADING è impostata, la stringa lParam viene letta nella direzione opposta dal testo \_ nella finestra padre. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) e **SB \_ GETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SB \_ SETTEXT**](sb-settext.md)
</dt> </dl>

 

 






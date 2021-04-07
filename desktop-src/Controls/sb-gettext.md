---
title: Messaggio SB_GETTEXT (COMmctrl. h)
description: Recupera il testo dalla parte specificata di una finestra di stato.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Controlli di Windows Message SB_GETTEXT
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
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048601"
---
# <a name="sb_gettext-message"></a>\_Messaggio SB GETtext

Recupera il testo dalla parte specificata di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte da cui recuperare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve il testo come stringa con terminazione null. Usare il messaggio [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per determinare la dimensione richiesta del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit costituito da valori a 2 16 bit. La parola low specifica la lunghezza, in caratteri, del testo. La parola alta specifica il tipo di operazione utilizzata per creare il testo. Il tipo può essere uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.<br/>  |
| <dl> <dt>**\_NOborders SBT**</dt> </dl>  | Il testo viene disegnato senza bordi.<br/>                                             |
| <dl> <dt>**\_POPOUT SBT**</dt> </dl>     | Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.<br/> |
| <dl> <dt>**\_RTLREADING SBT**</dt> </dl> | Il testo viene visualizzato nella direzione opposta del testo nella finestra padre.<br/>  |



 

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questo messaggio può compromettere la sicurezza del programma. Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer. Se si utilizza questo messaggio, chiamare prima [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere il numero di caratteri necessari e quindi chiamare il messaggio per recuperare la stringa. Se si attende prima di chiamare **SB \_ gettext** , il testo potrebbe cambiare, invalidando in tal modo il valore restituito di **SB \_ GETTEXTLENGTH**. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

Questo messaggio restituisce un massimo di 65.535 caratteri. Se la stringa di testo è più lunga, viene troncata.

Se il testo presenta il \_ tipo di disegno SBT OWNERDRAW, questo messaggio restituisce il valore a 32 bit associato al testo anziché la lunghezza e il tipo di operazione.

Normale testo visualizzato da sinistra a destra (LTR). È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL). Se \_ è impostata la RTLREADING SBT, la stringa *lParam* viene letta nella direzione opposta dal testo nella finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) e **SB \_ gettexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_testo SB**](sb-settext.md)
</dt> </dl>

 

 






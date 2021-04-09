---
title: Messaggio di EM_STOPGROUPTYPING (RichEdit. h)
description: Arresta un controllo Rich Edit dalla raccolta di azioni di tipizzazione aggiuntive nell'azione di annullamento corrente. Il controllo Archivia la successiva azione di tipizzazione, se presente, in una nuova azione nella coda di annullamento.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Controlli di Windows Message EM_STOPGROUPTYPING
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741234"
---
# <a name="em_stopgrouptyping-message"></a>\_Messaggio STOPGROUPTYPING em

Arresta un controllo Rich Edit dalla raccolta di azioni di tipizzazione aggiuntive nell'azione di annullamento corrente. Il controllo Archivia la successiva azione di tipizzazione, se presente, in una nuova azione nella coda di annullamento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero. Questo messaggio non può avere esito negativo.

## <a name="remarks"></a>Commenti

Un controllo Rich Edit consente di raggruppare azioni consecutive di tipizzazione, inclusi i caratteri eliminati tramite il tasto **BACKSPACE** , in una singola azione di annullamento fino a quando non si verifica uno degli eventi seguenti:

-   Il controllo riceve un **messaggio \_ STOPGROUPTYPING em** .
-   Il controllo perde lo stato attivo.
-   L'utente sposta la selezione corrente usando i tasti di direzione o facendo clic sul mouse.
-   L'utente preme il tasto **Canc** .
-   L'utente esegue qualsiasi altra azione, ad esempio un'operazione incolla che **non** implica la digitazione.

È possibile inviare il **messaggio \_ STOPGROUPTYPING em** per suddividere le azioni di digitazione consecutive in gruppi di annullamento più piccoli. Ad esempio, è possibile inviare **em \_ STOPGROUPTYPING** dopo ogni carattere o a ogni parola break.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Annulla**](em-undo.md)
</dt> </dl>

 

 






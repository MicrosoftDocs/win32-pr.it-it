---
title: TB_SAVERESTORE messaggio (Commctrl.h)
description: Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d04c16fda40bf66736431a684398eddf313529c669cc6db9ec49fbaad4f6f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168025"
---
# <a name="tb_saverestore-message"></a>TB \_ SAVERESTORE message

Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di salvataggio o ripristino. Se questo parametro è **TRUE,** le informazioni vengono salvate. Se è **FALSE,** le informazioni vengono ripristinate.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) che specifica la chiave del Registro di sistema, la sottochiave e il nome del valore per le informazioni sullo stato della barra degli strumenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per la versione 4.72 e precedenti, per usare questo messaggio per salvare o ripristinare una barra degli strumenti, la finestra padre del controllo barra degli strumenti deve implementare un gestore per il codice di notifica [ \_ TBN GETBUTTONINFO.](tbn-getbuttoninfo.md) La barra degli strumenti invia questa notifica per recuperare informazioni su ogni pulsante durante il ripristino.

La versione 5.80 include una nuova opzione di salvataggio/ripristino. All'inizio del processo e quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà una notifica [TBN \_ SAVE](tbn-save.md) o [TBN \_ RESTORE.](tbn-restore.md) Per usare questa opzione, è necessario implementare i gestori di notifica per fornire alla shell la bitmap e le informazioni sullo stato necessarie per salvare o ripristinare correttamente lo stato della barra degli strumenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 






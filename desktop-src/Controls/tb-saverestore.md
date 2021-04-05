---
title: Messaggio TB_SAVERESTORE (COMmctrl. h)
description: Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Controlli di Windows Message TB_SAVERESTORE
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
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873286"
---
# <a name="tb_saverestore-message"></a>TB \_ SAVERESTORE messaggio

Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag Save o Restore. Se questo parametro è **true**, le informazioni vengono salvate. Se è **false**, le informazioni vengono ripristinate.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) che specifica la chiave del registro di sistema, la sottochiave e il nome del valore per le informazioni sullo stato della barra degli strumenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per la versione 4,72 e versioni precedenti, per usare questo messaggio per salvare o ripristinare una barra degli strumenti, la finestra padre del controllo Toolbar deve implementare un gestore per il codice di notifica [ \_ GETBUTTONINFO di TBN](tbn-getbuttoninfo.md) . La barra degli strumenti Invia la notifica per recuperare le informazioni su ogni pulsante mentre viene ripristinato.

La versione 5,80 include una nuova opzione Salva/Ripristina. All'inizio del processo, quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà una notifica [TBN \_ Save](tbn-save.md) o [TBN \_ Restore](tbn-restore.md) . Per utilizzare questa opzione, è necessario implementare i gestori delle notifiche per fornire la shell con le informazioni sulla bitmap e sullo stato necessarie per salvare o ripristinare lo stato della barra degli strumenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 






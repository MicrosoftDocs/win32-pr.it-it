---
title: Messaggio di EM_FINDWORDBREAK (RichEdit. h)
description: Trova la parola successiva break prima o dopo la posizione del carattere specificata o recupera le informazioni sul carattere in quella posizione.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Controlli di Windows Message EM_FINDWORDBREAK
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477122"
---
# <a name="em_findwordbreak-message"></a>\_Messaggio FINDWORDBREAK em

Trova la parola successiva break prima o dopo la posizione del carattere specificata o recupera le informazioni sul carattere in quella posizione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'operazione di ricerca. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**\_classificazione WB**</dt> </dl>                | Restituisce la classe di caratteri e i flag di interruzioni di parola del carattere in corrispondenza della posizione specificata.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**delimitatore \_ WB**</dt> </dl>       | Restituisce **true** se il carattere in corrispondenza della posizione specificata è un delimitatore o **false** in caso contrario.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB a \_ sinistra**</dt> </dl>                            | Trova il carattere più vicino prima della posizione specificata che inizia con una parola.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**\_LEFTBREAK WB**</dt> </dl>             | Trova la parola finale successiva prima della posizione specificata. Questo valore è uguale a WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**\_MOVEWORDLEFT WB**</dt> </dl>    | Trova il carattere successivo che inizia una parola prima della posizione specificata. Questo valore viene usato durante l'elaborazione del tasto CTRL + freccia sinistra. Questo valore è simile a WB \_ MOVEWORDPREV. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**\_MOVEWORDRIGHT WB**</dt> </dl> | Trova il carattere successivo che inizia una parola dopo la posizione specificata. Questo valore viene usato durante l'elaborazione della chiave CTRL + right. Questo valore è simile a WB \_ MOVEWORDNEXT. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB a \_ destra**</dt> </dl>                         | Trova il carattere successivo che inizia una parola dopo la posizione specificata.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**\_RIGHTBREAK WB**</dt> </dl>          | Trova il successivo delimitatore di fine parola dopo la posizione specificata. Questo valore è uguale a WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione iniziale del carattere in base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce un valore basato sul parametro *wParam* .



| Codice restituito                                                                                    | Descrizione                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | Valore restituito<br/>                                                                                                |
| <dl> <dt>**\_classificazione WB**</dt> </dl>    | Restituisce la classe di caratteri e i flag di interruzioni di parola del carattere in corrispondenza della posizione specificata.<br/>                |
| <dl> <dt>**delimitatore \_ WB**</dt> </dl> | Restituisce **true** se il carattere in corrispondenza della posizione specificata è un delimitatore; in caso contrario, restituisce **false**.<br/> |
| <dl> <dt>**Altro**</dt> </dl>          | Restituisce l'indice dei caratteri della parola break.<br/>                                                              |



 

## <a name="remarks"></a>Commenti

Se *wParam* è WB \_ Left e WB \_ right, la procedura di Word break trova le interruzioni di parola solo dopo i delimitatori. Corrisponde alla funzionalità di un controllo di modifica. Se *wParam* è WB \_ MOVEWORDLEFT o WB \_ MOVEWORDRIGHT, la stored procedure di Word-break confronta anche le classi di caratteri e i flag di Word break.

Per informazioni sulle classi di caratteri e i flag di interruzione di parola, vedere [parole e interruzioni di riga](using-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






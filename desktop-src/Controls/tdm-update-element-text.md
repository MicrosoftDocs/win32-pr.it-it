---
title: TDM_UPDATE_ELEMENT_TEXT messaggio (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT messaggio: aggiorna un elemento di testo in una finestra di dialogo attività.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5abf6eb91b3eadfea71d0c9a4b5386e44db100c3a548998d5113636ff7f8cc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166914"
---
# <a name="tdm_update_element_text-message"></a>TDM \_ UPDATE ELEMENT TEXT \_ \_ message

Aggiorna un elemento di testo in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indica l'elemento da aggiornare. Per un'illustrazione degli elementi, vedere [Informazioni sui dialoghe attività.](task-dialogs-overview.md) Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                                           | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTENUTO \_ TDE**</dt> </dl>                                         | Contenuto.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**INFORMAZIONI ESPANSE DI TDE \_ \_**</dt> </dl> | Informazioni espanse.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**PIÈ DI PAGINA TDE \_**</dt> </dl>                                            | Testo del piè di pagina.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**ISTRUZIONE MAIN \_ TDE \_**</dt> </dl>             | Istruzione main.<br/>     |



 

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nuovo testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per evitare il ritaglio, il nuovo testo non deve essere più lungo del testo esistente. L'impostazione del testo su una stringa più breve non determina il ridimensionamento della finestra di dialogo.

Se il membro **pszExpandedInformation** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usato per creare la finestra di dialogo dell'attività è **NULL** e si invia un messaggio **TDM \_ UPDATE ELEMENT \_ \_ TEXT** con TDE EXPANDED INFORMATION, non si verifica \_ \_ nulla.

Il codice precedente si applica anche al piè di pagina e al piè di pagina \_ TDE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TESTO DELL'ELEMENTO SET TDM \_ \_ \_**](tdm-set-element-text.md)
</dt> </dl>

 

 






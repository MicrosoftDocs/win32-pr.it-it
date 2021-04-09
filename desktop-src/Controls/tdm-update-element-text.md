---
title: Messaggio TDM_UPDATE_ELEMENT_TEXT (COMmctrl. h)
description: Aggiorna un elemento di testo in una finestra di dialogo attività.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Controlli di Windows Message TDM_UPDATE_ELEMENT_TEXT
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
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121482"
---
# <a name="tdm_update_element_text-message"></a>\_Messaggio di \_ testo dell'elemento di aggiornamento TDM \_

Aggiorna un elemento di testo in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indica l'elemento da aggiornare. Per un'illustrazione degli elementi, vedere [informazioni sulle finestre di dialogo delle attività](task-dialogs-overview.md). Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                                           | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**contenuto Transparent Data Encryption \_**</dt> </dl>                                         | Contenuto.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informazioni espanse Transparent Data Encryption \_**</dt> </dl> | Informazioni espanse.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**piè di pagina Transparent Data Encryption \_**</dt> </dl>                                            | Testo del piè di pagina.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_istruzione principale di Transparent Data Encryption \_**</dt> </dl>             | Istruzione principale.<br/>     |



 

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nuovo testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per evitare il ritaglio, il nuovo testo non deve essere più lungo del testo esistente. Se si imposta il testo su una stringa più breve, la finestra di dialogo non verrà ridimensionata.

Se il membro **pszExpandedInformation** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usata per creare la finestra di dialogo attività era **null** e si invia un messaggio di **\_ \_ \_ testo dell'elemento di aggiornamento TDM** con \_ informazioni espanse su \_ Transparent Data Encryption, non viene eseguita alcuna operazione.

Quanto sopra si applica anche al piè di pagina di piè di pagina e di Data Encryption \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_testo dell' \_ elemento del set TDM \_**](tdm-set-element-text.md)
</dt> </dl>

 

 






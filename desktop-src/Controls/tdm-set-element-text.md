---
title: Messaggio TDM_SET_ELEMENT_TEXT (COMmctrl. h)
description: Aggiorna un elemento di testo in una finestra di dialogo attività.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Controlli di Windows Message TDM_SET_ELEMENT_TEXT
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048701"
---
# <a name="tdm_set_element_text-message"></a>\_Messaggio di \_ testo dell'elemento del set TDM \_

Aggiorna un elemento di testo in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indica l'elemento da aggiornare. Per un'illustrazione, vedere [informazioni sulle finestre di dialogo delle attività](task-dialogs-overview.md). Questo parametro deve essere uno dei valori seguenti.



| Valore                                                                                                                                                                                           | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**contenuto Transparent Data Encryption \_**</dt> </dl>                                         | Contenuto.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informazioni espanse Transparent Data Encryption \_**</dt> </dl> | Informazioni espanse.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**piè di pagina Transparent Data Encryption \_**</dt> </dl>                                            | Testo del piè di pagina.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_istruzione principale di Transparent Data Encryption \_**</dt> </dl>             | Istruzione principale.<br/>     |



 

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Nuovo testo da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Le dimensioni o il layout della finestra di dialogo attività possono variare in base al nuovo testo.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come impostare il testo del piè di pagina nella finestra di dialogo attività rappresentata da *HWND*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_testo dell' \_ elemento di aggiornamento TDM \_**](tdm-update-element-text.md)
</dt> </dl>

 

 






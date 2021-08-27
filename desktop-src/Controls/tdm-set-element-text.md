---
title: TDM_SET_ELEMENT_TEXT messaggio (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT: aggiorna un elemento di testo in una finestra di dialogo attività.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT dei controlli Windows messaggio
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
ms.openlocfilehash: 7bb0f81867bcff4fd5f7d533c156c8af17d0f4a761b6f8560aa584a85c62b7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060771"
---
# <a name="tdm_set_element_text-message"></a>TDM \_ SET ELEMENT TEXT \_ \_ message

Aggiorna un elemento di testo in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indica l'elemento da aggiornare. Per un'illustrazione, vedere [Informazioni sulle finestre di dialogo attività.](task-dialogs-overview.md) Questo parametro deve essere uno dei valori seguenti.



| Valore                                                                                                                                                                                           | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTENUTO \_ TDE**</dt> </dl>                                         | Contenuto.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**INFORMAZIONI TDE \_ \_ ESPANSE**</dt> </dl> | Informazioni espanse.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**PIÈ DI PAGINA \_ TDE**</dt> </dl>                                            | Testo del piè di pagina.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**ISTRUZIONE PRINCIPALE \_ TDE \_**</dt> </dl>             | Istruzione principale.<br/>     |



 

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Nuovo testo da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Le dimensioni o il layout della finestra di dialogo attività possono cambiare in base al nuovo testo.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come impostare il testo del piè di pagina nella finestra di dialogo attività rappresentata *da hwnd*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TESTO DELL'ELEMENTO \_ UPDATE \_ TDM \_**](tdm-update-element-text.md)
</dt> </dl>

 

 






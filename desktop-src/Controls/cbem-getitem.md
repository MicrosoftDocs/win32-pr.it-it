---
title: Messaggio CBEM_GETITEM (COMmctrl. h)
description: Ottiene le informazioni sugli elementi per un elemento ComboBoxEx specificato.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Controlli di Windows Message CBEM_GETITEM
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302298"
---
# <a name="cbem_getitem-message"></a>CBEM \_ messaggio GETitem

Ottiene le informazioni sugli elementi per un elemento ComboBoxEx specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che riceve le informazioni sull'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Quando il messaggio viene inviato, è necessario impostare i membri **iItem** e **mask** della struttura per indicare l'indice dell'elemento di destinazione e il tipo di informazioni da recuperare. Gli altri membri vengono impostati in base alle esigenze. Ad esempio, per recuperare il testo, è necessario impostare il \_ flag di testo CBEIF in **mask** e assegnare un valore a **cchTextMax**. Se si imposta il membro **iItem** su-1, verrà recuperato l'elemento visualizzato nel controllo di modifica.

Se il \_ flag di testo CBEIF è impostato nel membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto. Le applicazioni non devono presupporre che il testo venga sempre inserito nel buffer richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) e **CBEM \_ getitema** (ANSI)<br/>                 |



 

 






---
title: Messaggio CBEM_SETITEM (COMmctrl. h)
description: Imposta gli attributi per un elemento in un controllo ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Controlli di Windows Message CBEM_SETITEM
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743399"
---
# <a name="cbem_setitem-message"></a>CBEM- \_ messaggio di elemento

Imposta gli attributi per un elemento in un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contenente le informazioni sull'elemento da impostare. Quando il messaggio viene inviato, il membro **mask** della struttura deve essere impostato in modo da indicare quali attributi sono validi e il membro **iItem** deve specificare l'indice in base zero dell'elemento da modificare. Impostando il membro **iItem** su-1, l'elemento visualizzato nel controllo di modifica verrà modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ SETITEMW** (Unicode) e **CBEM \_ setitema** (ANSI)<br/>                 |



 

 






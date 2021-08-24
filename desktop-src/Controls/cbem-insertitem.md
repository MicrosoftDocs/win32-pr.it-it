---
title: CBEM_INSERTITEM messaggio (Commctrl.h)
description: Inserisce un nuovo elemento in un controllo ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699308"
---
# <a name="cbem_insertitem-message"></a>Messaggio INSERTITEM CBEM \_

Inserisce un nuovo elemento in un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che contiene informazioni sull'elemento da inserire. Quando il messaggio viene inviato, il **membro iItem** deve essere impostato per indicare l'indice in base zero in corrispondenza del quale inserire l'elemento. Per inserire un elemento alla fine dell'elenco, impostare il **membro iItem** su -1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in corrispondenza del quale il nuovo elemento è stato inserito in caso di esito positivo oppure -1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 






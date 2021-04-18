---
title: Messaggio CBEM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Controlli di Windows Message CBEM_INSERTITEM
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
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302646"
---
# <a name="cbem_insertitem-message"></a>\_Messaggio CBEM INSERTITEM

Inserisce un nuovo elemento in un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che contiene informazioni sull'elemento da inserire. Quando il messaggio viene inviato, è necessario impostare il membro **iItem** per indicare l'indice in base zero in corrispondenza del quale inserire l'elemento. Per inserire un elemento alla fine dell'elenco, impostare il membro **iItem** su-1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in corrispondenza del quale è stato inserito il nuovo elemento in caso di esito positivo; in caso contrario,-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 






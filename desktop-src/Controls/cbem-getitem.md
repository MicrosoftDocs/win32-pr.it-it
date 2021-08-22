---
title: CBEM_GETITEM messaggio (Commctrl.h)
description: Ottiene informazioni sull'elemento per un determinato elemento ComboBoxEx.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM dei messaggi Windows controlli
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
ms.openlocfilehash: dcf4dadf72a9f1fab679599c01c8fd0c6ca3541f2f77a5e8c52a740828966034
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528061"
---
# <a name="cbem_getitem-message"></a>Messaggio GETITEM CBEM \_

Ottiene informazioni sull'elemento per un determinato elemento ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che riceve le informazioni sull'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Quando il messaggio viene inviato, i membri **iItem** e **mask** della struttura devono essere impostati per indicare l'indice dell'elemento di destinazione e il tipo di informazioni da recuperare. Gli altri membri vengono impostati in base alle esigenze. Ad esempio, per recuperare testo, è necessario impostare il flag CBEIF TEXT nella maschera e assegnare \_ un valore a **cchTextMax**.  **L'impostazione del membro iItem** su -1 recupererà l'elemento visualizzato nel controllo di modifica.

Se il flag CBEIF TEXT è impostato nel membro mask della struttura \_ [**COMBOBOXEXITEM,**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto.  Le applicazioni non devono presupporre che il testo verrà sempre inserito nel buffer richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) e **CBEM \_ GETITEMA** (ANSI)<br/>                 |



 

 






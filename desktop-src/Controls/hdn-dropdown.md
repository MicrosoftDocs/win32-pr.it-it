---
title: HDN_DROPDOWN di notifica (Commctrl.h)
description: Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa sul controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a7e423c40fa655a9eca0e5b97c20a2d61add1e6c0b7f66b65a69afdc32a55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435571"
---
# <a name="hdn_dropdown-notification-code"></a>Codice di notifica a discesa HDN \_

Inviato da un controllo intestazione al relativo elemento padre quando si fa clic sulla freccia a discesa sul controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'esempio nella sezione Sintassi mostra come il ricevitore della notifica esegue il cast **di LPARAM** per recuperare la [**struttura NMHEADER.**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) **WPARAM** contiene l'ID del controllo che invia il messaggio.

Questo messaggio viene inviato solo se lo stile HDF \_ SPLITBUTTON è impostato sull'elemento di intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






---
title: TBN_GETOBJECT di notifica (Commctrl.h)
description: Inviato da un controllo barra degli strumenti che usa lo stile TBSTYLE REGISTERDROP per richiedere un oggetto destinazione di rilascio quando il puntatore \_ passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c50f3d403089ca7db42ab89232e57d68121424c066914c534ba13a826adb8ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876731"
---
# <a name="tbn_getobject-notification-code"></a>Codice di \_ notifica TBN GETOBJECT

Inviato da un controllo barra degli strumenti che usa lo stile [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che contiene informazioni sul pulsante che il puntatore ha passato e riceve i dati forniti dall'applicazione in risposta a questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che elabora questo codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della [**struttura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*. Il **membro pObject** deve essere impostato su un puntatore a oggetto valido e il membro **hResult** deve essere impostato su un flag di operazione riuscita. Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando si specifica un puntatore a un oggetto.

Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **NULL** e **hResult** su un flag di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






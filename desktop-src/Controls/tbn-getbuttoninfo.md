---
title: Codice di notifica TBN_GETBUTTONINFO (COMmctrl. h)
description: Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Controlli di Windows per il codice di notifica TBN_GETBUTTONINFO
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964625"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>\_Codice di notifica GETBUTTONINFO di TBN

Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Il membro **iItem** specifica un indice in base zero che fornisce un conteggio dei pulsanti nella finestra di dialogo Personalizza barra degli strumenti visualizzata come disponibile e presente sulla barra degli strumenti. Il membro **pszText** specifica l'indirizzo del testo del pulsante corrente e **cchText** ne specifica la lunghezza in caratteri. L'applicazione deve riempire la struttura con informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se le informazioni sul pulsante sono state copiate nella struttura specificata o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il controllo Toolbar alloca un buffer e il ricevitore (finestra padre) deve copiare il testo nel buffer. Il membro **cchText** contiene la lunghezza del buffer allocato dalla barra degli strumenti quando TBN \_ GETBUTTONINFO viene inviato alla finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) e **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 






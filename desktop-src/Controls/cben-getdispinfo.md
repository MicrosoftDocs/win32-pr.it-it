---
title: Codice di notifica CBEN_GETDISPINFO (COMmctrl. h)
description: Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- Controlli di Windows per il codice di notifica CBEN_GETDISPINFO
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517385"
---
# <a name="cben_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di CBEN

Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'elaborazione dell'applicazione del codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

La struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contiene una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Il membro **mask** specifica le informazioni richieste dal controllo.

Compilare i membri appropriati della struttura per restituire al controllo le informazioni richieste. Se il gestore di messaggi imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) su CBEIF \_ di un \_ elemento, il controllo archivia le informazioni e non le richiede di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ GETDISPINFOW** (Unicode) e **CBEN \_ GETDISPINFOA** (ANSI)<br/>         |



 

 






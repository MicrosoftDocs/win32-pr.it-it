---
title: Codice di notifica HDN_GETDISPINFO (COMmctrl. h)
description: Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento dell'intestazione di callback. Questo codice di notifica viene inviato come un \_ messaggio di notifica WM.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Controlli di Windows per il codice di notifica HDN_GETDISPINFO
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047937"
---
# <a name="hdn_getdispinfo-notification-code"></a>\_Codice di notifica GETDISPINFO di HDN

Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento dell'intestazione di callback. Questo codice di notifica viene inviato come un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) . In input i campi della struttura specificano le informazioni necessarie e l'elemento di interesse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un LRESULT.

## <a name="remarks"></a>Commenti

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo intestazione. Se il gestore di messaggi imposta il membro **mask** della struttura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) su HDI \_ di \_ SetItem, il controllo intestazione archivia le informazioni e non le richiede di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 






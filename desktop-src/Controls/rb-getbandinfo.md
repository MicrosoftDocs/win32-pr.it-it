---
title: Messaggio RB_GETBANDINFO (COMmctrl. h)
description: Recupera le informazioni su una banda specificata in un controllo Rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Controlli di Windows Message RB_GETBANDINFO
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120511"
---
# <a name="rb_getbandinfo-message"></a>\_Messaggio GETBANDINFO RB

Recupera le informazioni su una banda specificata in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per cui verranno recuperate le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che riceverà le informazioni sulla banda richiesta. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura sulla dimensione della struttura **REBARBANDINFO** e impostare il membro **fmask** sugli elementi che si desidera recuperare. Inoltre, è necessario impostare il **membro** REBARBANDINFO della struttura  sulla dimensione del buffer **lpText** quando \_ viene specificato il testo RBBIM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 






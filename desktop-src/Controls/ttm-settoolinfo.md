---
title: Messaggio TTM_SETTOOLINFO (COMmctrl. h)
description: Imposta le informazioni che un controllo ToolTip gestisce per uno strumento.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Controlli di Windows Message TTM_SETTOOLINFO
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478952"
---
# <a name="ttm_settoolinfo-message"></a>\_Messaggio TTM SETTOOLINFO

Imposta le informazioni che un controllo ToolTip gestisce per uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che specifica le informazioni da impostare. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Alcune proprietà interne di uno strumento vengono stabilite quando lo strumento viene creato e non vengono ricalcolate quando viene inviato un messaggio **TTM \_ SETTOOLINFO** . Se si assegnano semplicemente valori a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) e lo si passa al controllo ToolTip con un messaggio **\_ SETTOOLINFO di TTM** , queste proprietà potrebbero andare perse. Al contrario, l'applicazione deve prima richiedere la struttura **TOOLINFO** corrente dello strumento inviando la descrizione comando di un messaggio [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) . Modificare quindi i membri di questa struttura in base alle esigenze e passarli di nuovo al controllo ToolTip con **TTM \_ SETTOOLINFO**.

Quando si chiama **TTM \_ SETTOOLINFO**, la stringa a cui punta il membro **lpszText** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) non deve superare 80 **TCHARs** di lunghezza, incluso il **null** di terminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ SETTOOLINFOW** (Unicode) e **TTM \_ SETTOOLINFOA** (ANSI)<br/>           |



 

 






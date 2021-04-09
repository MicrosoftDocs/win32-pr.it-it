---
title: Messaggio CCM_GETVERSION (COMmctrl. h)
description: Ottiene il numero di versione di un controllo impostato dal messaggio della versione più recente di CCM \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Controlli di Windows Message CCM_GETVERSION
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120326"
---
# <a name="ccm_getversion-message"></a>\_Messaggio CCM GETversion

Ottiene il numero di versione di un controllo impostato dal messaggio della [**\_ versione**](ccm-setversion.md) più recente di CCM.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di versione impostato dal messaggio della [**\_ versione CCM**](ccm-setversion.md) più recente. Se non è stato inviato alcun messaggio di questo tipo, viene restituito zero.

## <a name="remarks"></a>Commenti

Questo messaggio non restituisce la versione della DLL. Per informazioni su come usare [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) per recuperare la versione corrente della dll, vedere [versioni della shell](common-control-versions.md) .

> [!Note]  
> Il numero di versione viene impostato su un controllo in base al controllo e potrebbe non essere lo stesso per tutti i controlli.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


---
title: CCM_GETVERSION messaggio (Commctrl.h)
description: Ottiene il numero di versione per un controllo impostato dal messaggio SETVERSION CCM \_ più recente.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION dei messaggi Windows controlli
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
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320261"
---
# <a name="ccm_getversion-message"></a>Messaggio \_ CCM GETVERSION

Ottiene il numero di versione per un controllo impostato dal messaggio [**\_ SETVERSION CCM più**](ccm-setversion.md) recente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di versione impostato dal messaggio [**\_ SETVERSION CCM più**](ccm-setversion.md) recente. Se tale messaggio non è stato inviato, restituisce zero.

## <a name="remarks"></a>Commenti

Questo messaggio non restituisce la versione della DLL. Per [informazioni su](common-control-versions.md) come usare [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) per recuperare la versione corrente della DLL, vedere Versioni della shell.

> [!Note]  
> Il numero di versione viene impostato su un controllo in base al controllo e potrebbe non essere lo stesso per tutti i controlli.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 


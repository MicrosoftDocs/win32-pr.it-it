---
description: Recupera l'handle per la barra dell'app di rilevamento automatico associata a un bordo dello schermo. Se il sistema dispone di più monitor, viene usato il monitoraggio che contiene la barra delle applicazioni principale.
title: ABM_GETAUTOHIDEBAR messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ce38caf8cc1ad39e682aa8650e08e4860a3406e33669008d6ceee65e0416149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051153"
---
# <a name="abm_getautohidebar-message"></a>Messaggio ABM \_ GETAUTOHIDEBAR

Recupera l'handle per la barra dell'app di rilevamento automatico associata a un bordo dello schermo. Se il sistema dispone di più monitor, viene usato il monitoraggio che contiene la barra delle applicazioni principale.

> [!Note]  
> Per eseguire una query per una barra delle app con rilevamento automatico su un monitoraggio specifico, usare [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo. È necessario specificare i **membri cbSize** **e uEdge** quando si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle alla barra dell'app di rilevamento automatico. Il valore restituito è **NULL** se si verifica un errore o se al bordo specificato non è associata alcuna barra dell'app con nascondimento automatico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 





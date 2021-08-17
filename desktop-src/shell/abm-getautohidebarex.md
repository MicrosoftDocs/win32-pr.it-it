---
description: Recupera l'handle per la barra dell'app con la visualizzazione automatica associata a un bordo dello schermo. Questo messaggio estende ABM GETAUTOHIDEBAR consentendo di specificare un determinato monitoraggio, da usare \_ in più situazioni di monitoraggio.
title: ABM_GETAUTOHIDEBAREX messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225240"
---
# <a name="abm_getautohidebarex-message"></a>Messaggio ABM \_ GETAUTOHIDEBAREX

Recupera l'handle per la barra dell'app con la visualizzazione automatica associata a un bordo dello schermo. Questo messaggio estende [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) consentendo di specificare un determinato monitoraggio, da usare in più situazioni di monitoraggio.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo e il monitoraggio. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **uEdge** e **rc.** tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle alla barra dell'app che si adatta automaticamente. Il valore restituito è **NULL** se si verifica un errore o se al bordo specificato del monitor specificato non è associata alcuna barra dell'app con la funzione dihide automatico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 





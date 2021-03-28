---
description: Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.
title: Messaggio ABM_GETAUTOHIDEBAR (Shellapi. h)
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
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128479"
---
# <a name="abm_getautohidebar-message"></a>\_Messaggio GETAUTOHIDEBAR ABM

Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.

> [!Note]  
> Per eseguire una query per un AppBar di Nascondi automaticamente su un monitor specifico, usare l' [**\_ GETAUTOHIDEBAREX ABM**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo. Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **uEdge** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il AppBar di Nascondi automaticamente. Il valore restituito è **null** se si verifica un errore o se non è associato alcun AppBar di Nascondi automaticamente al bordo specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETAUTOHIDEBAR ABM**](abm-setautohidebar.md)
</dt> <dt>

[**\_GETAUTOHIDEBAREX ABM**](abm-getautohidebarex.md)
</dt> <dt>

[**\_SETAUTOHIDEBAREX ABM**](abm-setautohidebarex.md)
</dt> </dl>

 

 





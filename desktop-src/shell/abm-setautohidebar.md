---
description: Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.
title: Messaggio ABM_SETAUTOHIDEBAR (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977450"
---
# <a name="abm_setautohidebar-message"></a>\_Messaggio SETAUTOHIDEBAR ABM

Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.

> [!Note]  
> Per registrare o annullare la registrazione di un AppBar di Nascondi automaticamente in un monitor specifico, usare l' [**\_ SETAUTOHIDEBAREX ABM**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Impostare il membro **lParam** su **true** per registrare AppBar o **false** per annullarne la registrazione. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **lParam** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se un AppBar di Nascondi automaticamente è già registrato per il bordo specificato.

## <a name="remarks"></a>Commenti

Il sistema consente un solo AppBar di Nascondi automaticamente per ogni bordo dello schermo. Questa operazione viene determinata quando viene impostato il membro **uEdge** della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETAUTOHIDEBAR ABM**](abm-getautohidebar.md)
</dt> <dt>

[**\_GETAUTOHIDEBAREX ABM**](abm-getautohidebarex.md)
</dt> <dt>

[**\_SETAUTOHIDEBAREX ABM**](abm-setautohidebarex.md)
</dt> </dl>

 

 





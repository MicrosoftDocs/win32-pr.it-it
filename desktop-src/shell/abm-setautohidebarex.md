---
description: Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Questo messaggio estende il \_ SETAUTOHIDEBAR ABM consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.
title: Messaggio ABM_SETAUTOHIDEBAREX (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996465"
---
# <a name="abm_setautohidebarex-message"></a>\_Messaggio SETAUTOHIDEBAREX ABM

Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Questo messaggio estende [**il \_ SETAUTOHIDEBAR ABM**](abm-setautohidebar.md) consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Impostare il membro **lParam** su **true** per registrare AppBar o **false** per annullarne la registrazione. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge**, **RC** e **lParam** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se un AppBar di Nascondi automaticamente è già registrato per il bordo specificato sul monitor specificato.

## <a name="remarks"></a>Commenti

Il sistema consente un solo AppBar di Nascondi automaticamente per ogni bordo di ogni monitor. Il monitoraggio è determinato dal membro **RC** e il bordo è determinato dal membro **UEdge** della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETAUTOHIDEBAR ABM**](abm-getautohidebar.md)
</dt> <dt>

[**\_GETAUTOHIDEBAREX ABM**](abm-getautohidebarex.md)
</dt> <dt>

[**\_SETAUTOHIDEBAR ABM**](abm-setautohidebar.md)
</dt> </dl>

 

 





---
description: Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Questo messaggio estende il \_ GETAUTOHIDEBAR ABM consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.
title: Messaggio ABM_GETAUTOHIDEBAREX (Shellapi. h)
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
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982971"
---
# <a name="abm_getautohidebarex-message"></a>\_Messaggio GETAUTOHIDEBAREX ABM

Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Questo messaggio estende [**il \_ GETAUTOHIDEBAR ABM**](abm-getautohidebar.md) consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo e il monitoraggio. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il AppBar di Nascondi automaticamente. Il valore restituito è **null** se si verifica un errore o se non è associato alcun AppBar di Nascondi automaticamente al bordo specificato del monitor specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETAUTOHIDEBAR ABM**](abm-getautohidebar.md)
</dt> <dt>

[**\_SETAUTOHIDEBAR ABM**](abm-setautohidebar.md)
</dt> <dt>

[**\_SETAUTOHIDEBAREX ABM**](abm-setautohidebarex.md)
</dt> </dl>

 

 





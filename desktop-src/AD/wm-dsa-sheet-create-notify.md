---
title: Messaggio WM_DSA_SHEET_CREATE_NOTIFY
description: Inviato allo snap-in MMC Active Directory per creare una finestra delle proprietà secondaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Messaggio WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964298"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>Creazione di un \_ \_ messaggio di \_ notifica del foglio DSA WM \_

Per creare una finestra delle proprietà secondaria, viene pubblicato il messaggio di **notifica del foglio DSA WM per Active Directory la creazione di un messaggio di \_ \_ \_ \_ notifica** .

> [!Note]  
> Il valore di questo messaggio non è definito in un file di intestazione pubblicato. Per utilizzare questo valore del messaggio, definirlo nel formato esatto visualizzato.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle della finestra dello snap-in che elaborerà questo messaggio. Questo handle viene ottenuto dal membro **hwndHidden** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntatore a una struttura di [**\_ informazioni della \_ pagina \_ DSA sec**](dsa-sec-page-info.md) che definisce la finestra delle proprietà secondaria da creare. Il ricevitore del messaggio deve liberare questa memoria con la funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando non è più necessaria.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**\_ \_ informazioni pagina di DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


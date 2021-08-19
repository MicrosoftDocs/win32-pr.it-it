---
title: WM_DSA_SHEET_CREATE_NOTIFY messaggio
description: Inviato nello snap-in MMC di Active Directory per creare una finestra delle proprietà secondaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY message Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024189"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>MESSAGGIO DI \_ NOTIFICA \_ CREAZIONE FOGLIO \_ WM DSA \_

Il **messaggio WM \_ DSA \_ SHEET CREATE \_ \_ NOTIFY** viene inviato nello snap-in MMC di Active Directory per creare una finestra delle proprietà secondaria.

> [!Note]  
> Questo valore del messaggio non è definito in un file di intestazione pubblicato. Per usare questo valore di messaggio, definirlo nel formato esatto visualizzato.

 


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

*Hwnd* 
</dt> <dd>

Handle della finestra dello snap-in che eelaborare il messaggio. Questo handle viene ottenuto dal **membro hwndHidden** della [**struttura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntatore a una [**struttura DSA \_ SEC PAGE \_ \_ INFO**](dsa-sec-page-info.md) che definisce la finestra delle proprietà secondaria da creare. Il ricevitore del messaggio deve liberare questa memoria [**con la funzione LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando non è più necessaria.

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

[**DSA SEC PAGE INFO (INFORMAZIONI PAGINA SEC \_ DSA) \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


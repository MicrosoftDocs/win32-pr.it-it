---
title: WM_DSA_SHEET_CLOSE_NOTIFY messaggio
description: Inviato nello snap-in MMC di Active Directory quando una finestra delle proprietà secondaria viene distrutta.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY message Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181674"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>MESSAGGIO DI \_ NOTIFICA CHIUSURA FOGLIO WM DSA \_ \_ \_

Il **messaggio WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY** viene inviato nello snap-in MMC di Active Directory quando una finestra delle proprietà secondaria viene distrutta.

> [!Note]  
> Questo valore del messaggio non è definito in un file di intestazione pubblicato. Per usare questo valore di messaggio, è necessario definirlo manualmente nel formato esatto visualizzato.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
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

Contiene un valore a 32 bit definito dall'applicazione. Questa operazione viene ottenuta **dal membro wParamSheetClose** della [**struttura PROPSHEETCFG.**](propsheetcfg.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 






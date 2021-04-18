---
title: Messaggio WM_DSA_SHEET_CLOSE_NOTIFY
description: Inserito nello snap-in di MMC Active Directory quando viene eliminata definitivamente una finestra delle proprietà secondaria.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Messaggio WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301710"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>\_Messaggio di \_ \_ notifica chiusura del foglio DSA WM \_

Il messaggio di **\_ notifica di \_ \_ chiusura \_ del foglio DSA WM** viene inserito nello snap-in di MMC Active Directory quando una finestra delle proprietà secondaria viene distrutta.

> [!Note]  
> Il valore di questo messaggio non è definito in un file di intestazione pubblicato. Per usare questo valore del messaggio, è necessario definirlo nel formato esatto indicato.

 


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

*HWND* 
</dt> <dd>

Handle della finestra dello snap-in che elaborerà questo messaggio. Questo handle viene ottenuto dal membro **hwndHidden** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un valore definito dall'applicazione a 32 bit. Questa operazione viene ottenuta dal membro **wParamSheetClose** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .

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

 

 






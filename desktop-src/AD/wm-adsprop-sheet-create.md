---
title: WM_ADSPROP_SHEET_CREATE messaggio
description: Inviato all'oggetto notifica per creare una finestra delle proprietà secondaria in uno snap-in MMC di Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE message Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ec88eaed682fd16fecb717b851b902d5ba52ce08d5360aa78b881a4b8cb4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024199"
---
# <a name="wm_adsprop_sheet_create-message"></a>Messaggio WM \_ ADSPROP \_ SHEET \_ CREATE

Il **messaggio WM \_ ADSPROP \_ SHEET \_ CREATE** viene inviato all'oggetto notifica per creare una finestra delle proprietà secondaria in uno snap-in MMC di Active Directory.

> [!Note]  
> Questo valore del messaggio non è definito in un file di intestazione pubblicato. Per usare questo valore di messaggio, è necessario definirlo manualmente nel formato esatto visualizzato.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle dell'oggetto notifica. Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntatore a una [**struttura DSA \_ SEC PAGE \_ \_ INFO**](dsa-sec-page-info.md) che definisce la pagina secondaria da creare. È possibile creare una sola finestra delle proprietà secondaria con il messaggio **WM \_ ADSPROP \_ SHEET \_ CREATE,** quindi la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) può contenere solo una [**struttura DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato. Deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio è sempre zero.

## <a name="remarks"></a>Commenti

Il chiamante deve allocare [**la struttura DSA \_ SEC PAGE \_ \_ INFO,**](dsa-sec-page-info.md) la stringa del titolo e tutte le stringhe [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) usando una singola chiamata alla [**funzione LocalAlloc.**](/windows/desktop/api/winbase/nf-winbase-localalloc) Il **messaggio WM \_ ADSPROP \_ SHEET \_ CREATE** è un messaggio asincrono, quindi verrà restituito prima della creazione del foglio secondario. Per questo problema, la memoria deve rimanere intatta dopo la fine del messaggio. Il ricevitore libera questa memoria con una singola chiamata alla [**funzione LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) dopo la creazione del foglio secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**DSA \_ SEC PAGE INFO (INFORMAZIONI PAGINA SEC DSA) \_ \_**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


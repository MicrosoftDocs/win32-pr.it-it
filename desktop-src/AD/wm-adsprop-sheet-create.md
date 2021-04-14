---
title: Messaggio WM_ADSPROP_SHEET_CREATE
description: Inviato all'oggetto notifica per creare una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517836"
---
# <a name="wm_adsprop_sheet_create-message"></a>\_Messaggio di \_ creazione del foglio ADSPROP WM \_

Per creare una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory, viene inviato un messaggio di **\_ creazione del \_ foglio \_ WM ADSPROP** all'oggetto notifica.

> [!Note]  
> Il valore di questo messaggio non è definito in un file di intestazione pubblicato. Per usare questo valore del messaggio, è necessario definirlo nel formato esatto indicato.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle dell'oggetto notifica. Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contiene un puntatore a una struttura di [**\_ informazioni della \_ pagina \_ DSA sec**](dsa-sec-page-info.md) che definisce la pagina secondaria da creare. È possibile creare una sola finestra delle proprietà secondaria con il messaggio di **\_ \_ \_ creazione del foglio WM ADSPROP** , quindi la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) può contenere una sola struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato. Deve essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio è sempre zero.

## <a name="remarks"></a>Commenti

Il chiamante deve allocare la struttura delle [**\_ \_ \_ informazioni della pagina DSA sec**](dsa-sec-page-info.md) , la stringa del titolo e tutte le stringhe [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) usando una singola chiamata alla funzione [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) . Il messaggio di **\_ creazione del \_ foglio \_ WM ADSPROP** è un messaggio asincrono, che verrà restituito prima della creazione del foglio secondario. Per questo motivo, la memoria deve rimanere intatta dopo la restituzione del messaggio. Il ricevitore libera questa memoria con una sola chiamata alla funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) dopo la creazione del foglio secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PARENTHWND DS \_ CFSTR**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**\_ \_ informazioni pagina di DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


---
title: Struttura PROPSHEETCFG
description: Usato per contenere i dati di configurazione della finestra delle proprietà.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Struttura PROPSHEETCFG Active Directory
- Puntatore alla struttura PPROPSHEETCFG Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 971296e1e269e977919f142d1efe24426b9c83f19ac26da2e2362ab48da0aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025439"
---
# <a name="propsheetcfg-structure"></a>Struttura PROPSHEETCFG

La **struttura PROPSHEETCFG** viene usata per contenere i dati di configurazione della finestra delle proprietà. Questa struttura è contenuta nel formato degli Appunti [**CFSTR \_ DS \_ PROPSHEETCONFIG.**](cfstr-ds-propsheetconfig.md)

> [!Note]  
> Questa struttura non è definita in un file di intestazione pubblicato. Per usare questa struttura, è necessario definirla manualmente nel formato esatto visualizzato.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Members

<dl> <dt>

**lNotifyHandle**
</dt> <dd>

Contiene l'handle di notifica. È identico all'handle passato per il *parametro handle* nel metodo [**IExtendPropertySheet2::CreatePropertyPages.**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85))

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Contiene l'handle di finestra della finestra delle proprietà padre.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Contiene l'handle della finestra nascosta.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Contiene un valore a 32 bit definito dall'applicazione. Questo valore viene passato nuovamente all'applicazione nel *parametro wParam* del messaggio [**WM \_ DSA \_ SHEET CLOSE \_ \_ NOTIFY.**](wm-dsa-sheet-close-notify.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**NOTIFICA \_ DI CHIUSURA DEL FOGLIO WM DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 


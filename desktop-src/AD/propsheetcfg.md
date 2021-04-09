---
title: Struttura PROPSHEETCFG
description: Utilizzato per contenere i dati di configurazione della finestra delle proprietà.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory della struttura PROPSHEETCFG
- Active Directory puntatore alla struttura PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048400"
---
# <a name="propsheetcfg-structure"></a>Struttura PROPSHEETCFG

La struttura **PROPSHEETCFG** viene utilizzata per contenere i dati di configurazione della finestra delle proprietà. Questa struttura è contenuta nel formato [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) Clipboard.

> [!Note]  
> Questa struttura non è definita in un file di intestazione pubblicato. Per usare questa struttura, è necessario definirla nel formato esatto illustrato.

 

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

Contiene l'handle di notifica. Si tratta di un handle identico a quello passato per il parametro *handle* nel metodo [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Contiene l'handle della finestra delle proprietà padre.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Contiene l'handle della finestra nascosta.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Contiene un valore definito dall'applicazione a 32 bit. Questo valore viene passato nuovamente all'applicazione nel *wParam* del messaggio di [**notifica di \_ \_ chiusura del \_ foglio \_ DSA WM**](wm-dsa-sheet-close-notify.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PROPSHEETCONFIG DS \_ CFSTR**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**\_notifica di \_ chiusura del foglio DSA \_ WM \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 


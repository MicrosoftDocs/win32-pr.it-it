---
title: CQPM_GETPARAMETERS messaggio (Cmnquery.h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per recuperare i dati sulla query eseguita dalla pagina.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS message Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64713c79fc2c1b72f1962363f1330ecd794ad804f0ab084b66c134c66133cd82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021232"
---
# <a name="cqpm_getparameters-message"></a>Messaggio CQPM \_ GETPARAMETERS

Il **messaggio CQPM \_ GETPARAMETERS** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per recuperare i dati sulla query eseguita dalla pagina.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**un valore LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) che riceve i dati sulla query eseguita dalla pagina. Se questo parametro è **NULL,** la **struttura DSQUERYPARAMS** deve essere allocata dall'estensione usando la [**funzione CoTaskMemAlloc.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S OK in \_ caso** di esito positivo o un codice **di errore HRESULT** standard in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**Cotaskmemalloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 


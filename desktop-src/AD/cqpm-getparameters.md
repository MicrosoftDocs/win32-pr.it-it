---
title: Messaggio CQPM_GETPARAMETERS (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una pagina di estensione del modulo di query per recuperare i dati relativi alla query eseguita dalla pagina.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_GETPARAMETERS Active Directory
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
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873441"
---
# <a name="cqpm_getparameters-message"></a>\_Messaggio GETparameters CQPM

Il messaggio **CQPM \_ GetParameters** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una pagina di estensione del modulo di query per recuperare i dati relativi alla query eseguita dalla pagina.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) che riceve i dati relativi alla query eseguita dalla pagina. Se questo parametro è **null**, la struttura **DSQUERYPARAMS** deve essere allocata dall'estensione utilizzando la funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se l'esito è positivo o un codice di errore **HRESULT** standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 


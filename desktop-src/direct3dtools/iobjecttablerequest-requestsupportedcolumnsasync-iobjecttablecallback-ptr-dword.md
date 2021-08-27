---
description: Richieste per ottenere informazioni sulle colonne (campi) supportate da questo tipo di richiesta di tabella di oggetti.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IObjectTableRequest::RequestSupportedColumnsAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bfdf3b488296cf0092f59d4b944c39e00df45e31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629584"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Metodo IObjectTableRequest::RequestSupportedColumnsAsync

Richieste per ottenere informazioni sulle colonne (campi) supportate da questo tipo di richiesta di tabella di oggetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*requestCallback*   
Indirizzo del callback utilizzato per notificare i risultati all'host.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IObjectTableRequest**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 

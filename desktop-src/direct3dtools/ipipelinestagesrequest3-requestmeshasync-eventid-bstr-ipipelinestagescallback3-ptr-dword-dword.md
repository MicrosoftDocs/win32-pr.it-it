---
description: Richiesta asincrona per ottenere i dati della mesh dall'evento specificato.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPipeLineStagesRequest3::RequestMeshAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ea2b5602d8668cec019efb02f4202dd7110da8cf
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623567"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest3::RequestMeshAsync

Richiesta asincrona per ottenere i dati della mesh dall'evento specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Eventid*   
Evento specificato.

*meshFilename*   
Stringa COM contenente il percorso del file in cui vengono scritti i dati della mesh.

*requestCallback*   
Indirizzo del callback utilizzato per notificare i risultati all'host.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesRequest3**](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 

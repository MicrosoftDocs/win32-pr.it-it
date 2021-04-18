---
description: Richiesta asincrona per ottenere un elenco di fasi usate per il frame e l'evento specificati.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest:: RequestSupportedStagesAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304309"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest:: RequestSupportedStagesAsync

Richiesta asincrona per ottenere un elenco di fasi usate per il frame e l'evento specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*NumeroFrame*   
Frame specificato.

*eventID*   
Evento specificato.

*requestCallback*   
Indirizzo del callback utilizzato per notificare all'host i risultati.

*requestCookie*   
Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesRequest**](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 

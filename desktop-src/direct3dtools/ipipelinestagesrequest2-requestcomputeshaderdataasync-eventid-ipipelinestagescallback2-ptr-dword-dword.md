---
description: Richiesta asincrona per ottenere i dati di compute shader per la distribuzione specificata.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest2:: RequestComputeShaderDataAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304308"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest2:: RequestComputeShaderDataAsync

Richiesta asincrona per ottenere i dati di compute shader per la distribuzione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*eventID*   
Evento di invio specificato.

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

[**IPipeLineStagesRequest2**](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 

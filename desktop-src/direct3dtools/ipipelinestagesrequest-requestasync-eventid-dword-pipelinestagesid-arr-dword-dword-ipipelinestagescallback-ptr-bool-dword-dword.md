---
description: Richiesta asincrona per ottenere le immagini di anteprima per la finestra delle fasi della pipeline grafica.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPipeLineStagesRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 890e0d95e811b47582a46ca0a1bc7a66dcbbb3fa5e6dab8a15d9e886730f22ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721778"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Metodo IPipeLineStagesRequest::RequestAsync

Richiesta asincrona per ottenere le immagini di anteprima per la finestra delle fasi della pipeline grafica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Eventid*   
ID dell'evento grafico per cui vengono richieste le immagini.

*numStages*   
Numero di fasi della pipeline per cui vengono richieste le immagini.

*count1 \_ stageIds*   
ID delle fasi della pipeline per cui vengono richieste le immagini.

*Larghezza*   
Larghezza delle immagini richieste.

*Altezza*   
Altezza delle immagini richieste.

*requestCallback*   
Indirizzo del callback utilizzato per notificare i risultati all'host.

*getMeshData*   
true per restituire i dati della mesh; in caso contrario, false.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesRequest**](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 

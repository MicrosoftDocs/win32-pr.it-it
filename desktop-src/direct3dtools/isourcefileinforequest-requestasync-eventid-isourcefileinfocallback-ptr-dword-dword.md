---
description: Richiesta asincrona per ottenere i file di origine associati al callstack di un evento.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo ISourceFileInfoRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: af2b1b924bd10afce3172ec0119c864fe4f7349c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624157"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Metodo ISourceFileInfoRequest::RequestAsync

Richiesta asincrona per ottenere i file di origine associati al callstack di un evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Eventid*   
Evento specificato.

*requestCallback*   
Indirizzo del callback utilizzato per inviare una notifica all'host dei risultati.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**ISourceFileInfoRequest**](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 

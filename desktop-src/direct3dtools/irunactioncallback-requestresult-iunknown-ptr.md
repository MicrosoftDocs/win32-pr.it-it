---
description: Funzione di callback usata per inviare una notifica all'host dei risultati da un'azione (ad esempio, acquisire un frame) richiesta.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IRunActionCallback::RequestResult
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e806a95515a59176c1070b573763a8581f40397
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627557"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>Metodo IRunActionCallback::RequestResult

Funzione di callback usata per inviare una notifica all'host dei risultati da un'azione (ad esempio, acquisire un frame) richiesta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a>Parametri

*Actionresult*   
Risultato dell'azione.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IRunActionCallback**](/windows/desktop/direct3dtools/irunactioncallback)

 

 

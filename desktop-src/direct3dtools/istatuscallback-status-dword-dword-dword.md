---
description: Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dei motori. Questo consente anche all'host di determinare che il motore è ancora in esecuzione.
title: Metodo IStatusCallback::Status
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622307"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Metodo IStatusCallback::Status

Funzione di callback utilizzata per notificare all'host lo stato di avanzamento del motore. Questo consente anche all'host di determinare che il motore è ancora in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Parametri

*dwMillisecondsElapsed*   
Tempo trascorso dall'ultima chiamata a Status, in millisecondi.

*dwFramesCaptured*   
Numero di frame acquisiti dall'ultima chiamata a Status.

*dwFramesElapsed*   
Numero di frame trascorsi dall'ultima chiamata a Status.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, **restituisce** S_OK . In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 

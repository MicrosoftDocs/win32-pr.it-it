---
description: Callback che notifica all'host quali fasi della pipeline non sono in grado di restituire dati mesh per l'evento specificato nella richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPipeLineStagesCallback::MeshDataNotAvailableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622137"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Metodo IPipeLineStagesCallback::MeshDataNotAvailableCallback

Callback che notifica all'host quali fasi della pipeline non sono in grado di restituire dati mesh per l'evento specificato nella richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Parametri

*numberStages*   
Numero di errori di fase restituiti.

*Errori \_ count0*   
Errori della fase della pipeline.

*Larghezza*   
Larghezza della catena di scambio associato alla chiamata di disegno. Viene usato quando si richiedono immagini di anteprima della pipeline.

*Altezza*   
Altezza della catena di scambio associato alla chiamata di disegno. Viene usato quando si richiedono immagini di anteprima della pipeline.

*Eid*   
Evento rappresentato nei risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

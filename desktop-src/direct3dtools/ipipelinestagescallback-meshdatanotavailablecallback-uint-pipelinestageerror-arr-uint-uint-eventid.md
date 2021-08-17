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
ms.openlocfilehash: 41fbedaa6deaf2a799f8d721309bfbe1b44bc2110dfae0a3cf30a4afbe0fa1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276081"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

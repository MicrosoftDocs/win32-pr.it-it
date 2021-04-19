---
description: Funzione di callback utilizzata per notificare all'host lo stato di avanzamento dei motori. Questa operazione funge anche da metodo per l'host per determinare che il motore è ancora in esecuzione.
title: 'Metodo IStatusCallback:: status'
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
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304294"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Metodo IStatusCallback:: status

Funzione di callback utilizzata per notificare all'host lo stato del motore. Questa operazione funge anche da metodo per l'host per determinare che il motore è ancora in esecuzione.

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
Tempo trascorso dall'ultima chiamata allo stato, in millisecondi.

*dwFramesCaptured*   
Numero di frame acquisiti dall'ultima chiamata allo stato.

*dwFramesElapsed*   
Il numero di fotogrammi trascorsi dall'ultima chiamata allo stato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 

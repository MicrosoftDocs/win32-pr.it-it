---
description: Callback che notifica all'host le informazioni sull'immagine delle fasi della pipeline restituite dalla richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342046"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>Metodo IPipeLineStagesCallback:: ResultCallback

Callback che notifica all'host le informazioni sull'immagine delle fasi della pipeline restituite dalla richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a>Parametri

*stageId*   
Fase della pipeline rappresentata nei risultati.

*Eid*   
Evento rappresentato nei risultati.

*Larghezza*   
Larghezza dell'immagine di visualizzazione della pipeline.

*altezza*   
Altezza dell'immagine della visualizzazione della pipeline.

*formato*   
Formato dell'immagine di visualizzazione della pipeline.

*dimensioni*   
Dimensione dell'immagine in byte.

*\_buffer count5*   
Immagine della visualizzazione della pipeline.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

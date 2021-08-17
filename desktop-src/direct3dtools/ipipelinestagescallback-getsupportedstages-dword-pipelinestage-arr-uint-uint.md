---
description: Callback che notifica all'host quali fasi della pipeline vengono usate dalla chiamata di disegno della richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPipeLineStagesCallback::GetSupportedStages
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789158dda43ef3fcb8ead982c38b15f4bd26cb7c8fb291a841d529d8c6dad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405941"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Metodo IPipeLineStagesCallback::GetSupportedStages

Callback che notifica all'host quali fasi della pipeline vengono usate dalla chiamata di disegno della richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a>Parametri

*Numcolumns*   
Numero di fasi restituite.

*count0 \_ pStages*   
Fasi della pipeline.

*swapChainWidth*   
Larghezza della catena di scambio associato alla chiamata di disegno. Viene usato quando si richiedono immagini di anteprima della pipeline.

*swapChainHeight*   
Altezza della catena di scambio associato alla chiamata di disegno. Viene usato quando si richiedono immagini di anteprima della pipeline.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

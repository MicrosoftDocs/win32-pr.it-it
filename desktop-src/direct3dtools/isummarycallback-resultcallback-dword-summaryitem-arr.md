---
description: Funzione di callback utilizzata per notificare all'host le informazioni di riepilogo del log di grafica.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISummaryCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304292"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Metodo ISummaryCallback:: ResultCallback

Funzione di callback utilizzata per notificare all'host le informazioni di riepilogo del log di grafica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a>Parametri

*conteggio*   
Numero di elementi di informazioni di riepilogo restituiti.

*\_summaryItem count0*   
Elementi di informazioni di riepilogo (coppie chiave-valore).

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**ISummaryCallback**](/windows/desktop/direct3dtools/isummarycallback)

 

 

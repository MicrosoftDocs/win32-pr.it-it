---
description: Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di un istogramma.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine5Callbacks:: LoadHistogramComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0e468422f722a8bd549d63f34225833462856b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304187"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>Metodo IPixEngine5Callbacks:: LoadHistogramComplete

Funzione di callback utilizzata per notificare all'host quando è stato completato il caricamento di un istogramma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*istogramma*   
Indirizzo dei dati dell'istogramma per l'istogramma caricato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 

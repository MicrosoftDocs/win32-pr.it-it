---
description: Richieste di annullamento della generazione di istruzioni di traccia dello shader in una richiesta di debug.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderCancel:: CancelGenerate'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304036"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Metodo IDebugShaderCancel:: CancelGenerate

Richieste di annullamento della generazione di istruzioni di traccia dello shader in una richiesta di debug.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a>Parametri

*requestInfo*   
Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.

*pPixelHistory*   
Indirizzo dei risultati della Cronologia pixel utilizzati per trovare il pixel associato di cui eseguire il debug. Si applica solo quando si esegue il debug di un pixel shader.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugShaderCancel**](/windows/desktop/direct3dtools/idebugshadercancel)

 

 

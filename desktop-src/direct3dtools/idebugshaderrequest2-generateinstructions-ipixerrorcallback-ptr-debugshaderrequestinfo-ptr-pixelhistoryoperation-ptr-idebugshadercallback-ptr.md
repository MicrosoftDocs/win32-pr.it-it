---
description: Richiede la generazione di istruzioni di traccia dello shader in una richiesta di debug. Il debug basato su traccia si verifica sulla CPU (Warp) invece che sulla GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderRequest2:: GenerateInstructions'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521858"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Metodo IDebugShaderRequest2:: GenerateInstructions

Richiede la generazione di istruzioni di traccia dello shader in una richiesta di debug. Il debug basato su traccia si verifica sulla CPU (Warp) invece che sulla GPU.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Parametri

*errorCallback*   
Indirizzo di un callback per gli errori che potrebbero verificarsi durante la generazione di istruzioni di traccia dello shader.

*requestInfo*   
Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.

*pPixelHistory*   
Indirizzo dei risultati della Cronologia pixel utilizzati per trovare il pixel associato di cui eseguire il debug. Si applica solo quando si esegue il debug di un pixel shader.

*pCallback*   
Indirizzo di un callback utilizzato per notificare all'host i risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 

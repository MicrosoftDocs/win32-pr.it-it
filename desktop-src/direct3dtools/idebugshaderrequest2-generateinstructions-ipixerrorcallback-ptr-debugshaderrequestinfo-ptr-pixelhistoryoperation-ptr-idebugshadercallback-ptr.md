---
description: Richieste di generazione di istruzioni di traccia shader in una richiesta di debug. Il debug basato su traccia si verifica nella CPU (warp) anziché nella GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IDebugShaderRequest2::GenerateInstructions
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
ms.openlocfilehash: f3af0e624435c03416db0bf8d74bc3aa8418ae78
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625157"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Metodo IDebugShaderRequest2::GenerateInstructions

Richieste di generazione di istruzioni di traccia shader in una richiesta di debug. Il debug basato su traccia si verifica nella CPU (warp) anziché nella GPU.

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

*Requestinfo*   
Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.

*pPixelHistory*   
Indirizzo dei risultati della cronologia dei pixel usati per trovare il pixel associato di cui eseguire il debug. Si applica solo quando si esegue il debug di pixel shader.

*pCallback*   
Indirizzo di un callback utilizzato per inviare una notifica all'host dei risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 

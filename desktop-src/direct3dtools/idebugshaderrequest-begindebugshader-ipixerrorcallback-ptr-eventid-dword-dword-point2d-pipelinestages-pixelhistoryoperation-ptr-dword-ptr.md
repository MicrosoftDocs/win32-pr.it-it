---
description: Richiede di avviare una sessione di debug dello shader per la fase della pipeline, il pixel/vertice, se applicabile, l'evento e il frame specificati.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IDebugShaderRequest::BeginDebugShader
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629855"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Metodo IDebugShaderRequest::BeginDebugShader

Richiede di avviare una sessione di debug dello shader per la fase della pipeline, il pixel/vertice, se applicabile, l'evento e il frame specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Parametri

*errorCallback*   
Indirizzo di un callback per gli errori che potrebbero verificarsi durante il debug.

*Eventid*   
Evento specificato.

*frameNumber*   
Frame specificato.

*Vertice*   
Vertice specificato. Si applica solo quando si esegue il debug di un vertex shader.

*pixel*   
Pixel specificato. Si applica solo quando si esegue il debug di pixel shader.

*Palco*   
Fase della pipeline specificata.

*pPixelHistory*   
Indirizzo dei risultati della cronologia pixel usati per trovare il pixel associato di cui eseguire il debug. Si applica solo quando si esegue il debug di pixel shader.

*pDevice*   
Indirizzo da passare al motore di debug per la comunicazione con questa sessione di debug (readprocessmemory del motore di debug in questo indirizzo).

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 

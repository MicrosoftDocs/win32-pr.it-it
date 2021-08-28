---
description: Richieste di debug di uno shader nella GPU (debug in tempo reale) rispetto alla CPU (debug basato su traccia).
MS-HAID: vspixengine.IDebugLiveShaderRequest\_BeginDebugLiveShader\_DebugShaderRequestInfo\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IDebugLiveShaderRequest::BeginDebugLiveShader
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 805B2B68-C251-4192-85A3-F857B3F204C7
api_name:
- IDebugLiveShaderRequest.BeginDebugLiveShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d78260dd35e5ca0aed2b8e89f1fc37f76ecba3a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627147"
---
# <a name="span-idvspixengineidebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptrspanidebugliveshaderrequestbegindebugliveshader-method"></a><span id="vspixengine.idebugliveshaderrequest_begindebugliveshader_debugshaderrequestinfo_ptr"></span>Metodo IDebugLiveShaderRequest::BeginDebugLiveShader

Richieste di debug di uno shader nella GPU (debug in tempo reale) rispetto alla CPU (debug basato su traccia).

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginDebugLiveShader(
   DebugShaderRequestInfo * requestInfo
);
```

## <a name="parameters"></a>Parametri

*Requestinfo*   
Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugLiveShaderRequest**](/windows/desktop/direct3dtools/idebugliveshaderrequest)

 

 

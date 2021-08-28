---
description: Richiede di annullare la generazione di istruzioni di traccia shader in una richiesta di debug.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IDebugShaderCancel::CancelGenerate
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
ms.openlocfilehash: 320eb64057ac078fc31851021f73b445094f8ab7
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632159"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Metodo IDebugShaderCancel::CancelGenerate

Richiede di annullare la generazione di istruzioni di traccia shader in una richiesta di debug.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a>Parametri

*Requestinfo*   
Indirizzo di una struttura DebugShaderRequestInfo che descrive l'evento/vertice/pixel richiesto.

*pPixelHistory*   
Indirizzo dei risultati della cronologia pixel usati per trovare il pixel associato di cui eseguire il debug. Si applica solo quando si esegue il debug di pixel shader.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IDebugShaderCancel**](/windows/desktop/direct3dtools/idebugshadercancel)

 

 

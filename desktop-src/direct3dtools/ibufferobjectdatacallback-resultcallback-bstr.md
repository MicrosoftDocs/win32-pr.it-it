---
description: Callback che notifica all'host le informazioni sul buffer scritte in un file dalla richiesta ascaited.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IBufferObjectDataCallback::ResultCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eaf084402c1cc34bff83d3b50002fbdcf3d97fb1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623097"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Metodo IBufferObjectDataCallback::ResultCallback

Callback che notifica all'host le informazioni sul buffer scritte in un file dalla richiesta ascaited.

## <a name="syntax"></a>Sintassi

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Parametri

*File* Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 

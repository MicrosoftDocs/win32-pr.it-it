---
description: Callback che notifica all'host di informazioni sul buffer scritte in un file dalla richiesta assocaited.
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
ms.openlocfilehash: 3a1ece7d54ccc27a91f47cb6d5cad1c2ff5861a038c10ed42d83eceef67fb4a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406211"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Metodo IBufferObjectDataCallback::ResultCallback

Callback che notifica all'host di informazioni sul buffer scritte in un file dalla richiesta assocaited.

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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 

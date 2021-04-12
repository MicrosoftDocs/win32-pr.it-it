---
description: Callback che notifica all'host le informazioni del buffer scritte in un file dalla richiesta associata.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IBufferObjectDataCallback:: ResultCallback'
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
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401336"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Metodo IBufferObjectDataCallback:: ResultCallback

Callback che notifica all'host le informazioni del buffer scritte in un file dalla richiesta associata.

## <a name="syntax"></a>Sintassi

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Parametri

*File* Stringa COM che contiene il percorso del file in cui vengono scritti i risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 

---
description: Callback che notifica all'host le informazioni di buffer generico restituite dalla richiesta associata.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IGenericBufferDataCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747151"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Metodo IGenericBufferDataCallback:: ResultCallback

Callback che notifica all'host le informazioni di buffer generico restituite dalla richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a>Parametri

*dimensioni*   
Dimensioni in byte del contenuto del buffer.

*\_buffer count0*   
Contenuto del buffer. Nella maggior parte dei casi si tratta di dati XML.

*tipo*   
Stringa COM che indica il tipo di contenuto restituito nel buffer.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IGenericBufferDataCallback**](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 

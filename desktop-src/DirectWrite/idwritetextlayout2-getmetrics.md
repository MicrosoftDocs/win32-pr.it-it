---
title: Metodo IdWriteTextLayout2 GetMetrics
description: Recupera le metriche complessive per la stringa formattata.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Metodo GetMetrics Direct Write
- Metodo GetMetrics Direct Write, interfaccia IDWriteTextLayout2
- Interfaccia IDWriteTextLayout2 Scrittura diretta, metodo GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f08a0b1e47003bb818f0b80ebc3b13f639f8ded8334137d8b8812e7f0154a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070741"
---
# <a name="idwritetextlayout2getmetrics-method"></a>Metodo IDWriteTextLayout2::GetMetrics

Recupera le metriche complessive per la stringa formattata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *textMetrics* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\***

Quando questo metodo viene restituito, contiene le distanze misurate del testo e del contenuto associato dopo la formattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 






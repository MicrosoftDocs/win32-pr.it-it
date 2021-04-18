---
description: Imposta l'esempio per l'origine del flusso multimediale.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Metodo IMFMediaStreamSourceSampleRequest:: sesample'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320681"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a>Metodo IMFMediaStreamSourceSampleRequest:: sesample

Imposta l'esempio per l'origine del flusso multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Esempio per l'origine del flusso multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaStreamSourceSampleRequest**](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 





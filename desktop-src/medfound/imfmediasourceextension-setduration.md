---
description: Imposta la durata dell'origine multimediale in unità di 100 nanosecondi.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: Metodo IMFMediaSourceExtension::SetDuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061211"
---
# <a name="imfmediasourceextensionsetduration-method"></a>Metodo IMFMediaSourceExtension::SetDuration

Imposta la durata dell'origine multimediale in unità di 100 nanosecondi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*durata* \[ Pollici\]
</dt> <dd>

Durata dell'origine multimediale in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





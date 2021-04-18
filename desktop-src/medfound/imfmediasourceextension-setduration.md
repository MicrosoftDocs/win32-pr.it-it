---
description: Imposta la durata dell'origine multimediale in unità 100-nanosecondi.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Metodo IMFMediaSourceExtension:: seduration'
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
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320682"
---
# <a name="imfmediasourceextensionsetduration-method"></a>Metodo IMFMediaSourceExtension:: seduration

Imposta la durata dell'origine multimediale in unità 100-nanosecondi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*durata* \[ in\]
</dt> <dd>

Durata dell'origine del supporto in unità 100-nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





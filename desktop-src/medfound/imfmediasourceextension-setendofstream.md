---
description: Indicare che è stata raggiunta la fine del flusso multimediale.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: Metodo IMFMediaSourceExtension::SetEndOfStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 29937a939dd8d087e1a70224950ddd8d14eea8989127dc9f33c2747468db4b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062970"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>Metodo IMFMediaSourceExtension::SetEndOfStream

Indicare che è stata raggiunta la fine del flusso multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errore* \[ Pollici\]
</dt> <dd>

Usato per passare le informazioni sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[**ERRORE MF \_ MSE \_**](mf-mse-error.md)
</dt> </dl>

 

 





---
description: Indica che è stata raggiunta la fine del flusso multimediale.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Metodo IMFMediaSourceExtension:: SetEndOfStream'
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
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320683"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>Metodo IMFMediaSourceExtension:: SetEndOfStream

Indica che è stata raggiunta la fine del flusso multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errore* \[ in\]
</dt> <dd>

Utilizzato per passare le informazioni sull'errore.

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
</dt> <dt>

[**\_errore MF MSE \_**](mf-mse-error.md)
</dt> </dl>

 

 





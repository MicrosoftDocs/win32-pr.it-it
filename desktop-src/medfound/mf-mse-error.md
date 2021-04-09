---
description: Definisce i diversi Stati di errore dell'estensione di origine multimediale.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Enumerazione MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130718"
---
# <a name="mf_mse_error-enumeration"></a>\_ \_ Enumerazione errori MF MSE

Definisce i diversi Stati di errore dell'estensione di origine multimediale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_errore MF \_ MSE \_ NOERROR**
</dt> <dd>

Non specifica alcun errore.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_rete di \_ errori MF MSE \_**
</dt> <dd>

Specifica un errore con la rete.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ decodifica errore MF \_ MSE**
</dt> <dd>

Specifica un errore di decodifica.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**errore di MF \_ MSE \_ \_ sconosciuto \_**
</dt> <dd>

Specifica un errore sconosciuto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 





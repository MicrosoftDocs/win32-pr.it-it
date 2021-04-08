---
description: Definisce i diversi stati pronti dell'estensione di origine multimediale.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Enumerazione MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882229"
---
# <a name="mf_mse_ready-enumeration"></a>\_ \_ Enumerazione Ready di MF MSE

Definisce i diversi stati pronti dell'estensione di origine multimediale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**pronto per MF \_ MSE \_ \_ chiuso**
</dt> <dd>

Il codice sorgente multimediale è chiuso.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**pronto per l'uso di MF \_ MSE \_ \_**
</dt> <dd>

L'origine multimediale è aperta.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**fine del supporto per MF \_ MSE \_ \_**
</dt> <dd>

L'origine multimediale è terminata.

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

 

 





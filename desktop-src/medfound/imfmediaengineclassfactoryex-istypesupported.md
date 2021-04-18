---
description: Ottiene un valore che indica se il sistema di chiavi specificato supporta il tipo di supporto specificato.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'Metodo IMFMediaEngineClassFactoryEx:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320473"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>Metodo IMFMediaEngineClassFactoryEx:: IsTypeSupported

Ottiene un valore che indica se il sistema di chiavi specificato supporta il tipo di supporto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* 
</dt> <dd>

Tipo MIME per cui verificare il supporto.

</dd> <dt>

*Sistema* 
</dt> <dd>

Sistema di chiavi di cui verificare il supporto.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** se il tipo è supportato da un *sistema*. in caso contrario, **false.**

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

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 





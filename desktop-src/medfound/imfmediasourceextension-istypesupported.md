---
description: Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine multimediale.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: Metodo IMFMediaSourceExtension::IsTypeSupported
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974340"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>Metodo IMFMediaSourceExtension::IsTypeSupported

Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine multimediale.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Tipo di supporto per cui verificare il supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**true** se il tipo di supporto è supportato; in caso contrario, **false.**

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

 

 





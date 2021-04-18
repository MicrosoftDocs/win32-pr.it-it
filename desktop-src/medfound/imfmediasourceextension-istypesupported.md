---
description: Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine supporto.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Metodo IMFMediaSourceExtension:: IsTypeSupported'
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
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320684"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>Metodo IMFMediaSourceExtension:: IsTypeSupported

Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine supporto.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Tipo di supporto per cui verificare il supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**true** se il tipo di supporto è supportato. in caso contrario, **false**.

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

 

 





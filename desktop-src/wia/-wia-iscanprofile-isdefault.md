---
description: Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo IWiaItem2 associato.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Metodo IScanProfile:: IsDefault (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966841"
---
# <a name="iscanprofileisdefault-method"></a>Metodo IScanProfile:: IsDefault

Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbDefault* \[ out\]
</dt> <dd>

Tipo: **bool \** _

Puntatore a _ * BOOL * *.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE**


</dt> <dd>

Il profilo è il valore predefinito.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE**


</dt> <dd>

Il profilo non è il valore predefinito.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

*pbDefault* è **true** se il profilo contiene un `<Default>` elemento. È **false** se tale elemento non è presente. L'elemento non ha alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





---
description: Restituisce l'ID del dispositivo.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: Metodo IScanProfile::GetDeviceID (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 484c9a53542b0f7b62c00ca030b4bee9276914dce28bd3034865f308ba80705e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007611"
---
# <a name="iscanprofilegetdeviceid-method"></a>Metodo IScanProfile::GetDeviceID

Restituisce l'ID del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrDeviceID* \[ Cambio\]
</dt> <dd>

Tipo: **BSTR \***

Puntatore all'ID dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





---
description: Ottiene il numero di profili di analisi per il dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: Metodo IScanProfileMgr::GetNumProfilesforDeviceID (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c2af1e4bc73afee090d947e6bcca0060521cb15cf2faff06be8c9a893534ea4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264391"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>Metodo IScanProfileMgr::GetNumProfilesforDeviceID

Ottiene il numero di profili di analisi per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

ID del dispositivo.

</dd> <dt>

*pulNumProfiles* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Puntatore al numero di profili disponibili per il dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





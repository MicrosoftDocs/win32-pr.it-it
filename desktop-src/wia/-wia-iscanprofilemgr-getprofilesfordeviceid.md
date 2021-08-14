---
description: Ottiene tutti i profili di analisi associati a un dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: Metodo IScanProfileMgr::GetProfilesforDeviceID (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 8ca150d02aff2f84becf8b36aca87e2da24b2b83c9ccd85c0cf5a1c5ced0d664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209057"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>Metodo IScanProfileMgr::GetProfilesforDeviceID

Ottiene tutti i profili di analisi associati a un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

ID del dispositivo.

</dd> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Quando viene passato, un puntatore al numero massimo di profili da restituire. Quando viene restituito, puntatore a al numero di profili restituiti.

</dd> <dt>

*ppScanProfile* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Indirizzo di un puntatore a una matrice di profili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il numero totale di profili associati al dispositivo è inferiore al valore passato a *pulNumProfiles,* *pulNumProfiles* restituisce tale totale. In caso contrario, restituisce lo stesso valore passato.

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

 

 





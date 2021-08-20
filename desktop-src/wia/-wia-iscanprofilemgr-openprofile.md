---
description: Apre un profilo di analisi salvato su disco come file XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: Metodo IScanProfileMgr::OpenProfile (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 67b47fb6c905048b9906ce79a604beb463ca4947d4543cd5bb3e961545856428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670244"
---
# <a name="iscanprofilemgropenprofile-method"></a>Metodo IScanProfileMgr::OpenProfile

Apre un profilo di analisi salvato su disco come file XML.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guid* \[ Pollici\]
</dt> <dd>

Tipo: **GUID**

GUID del profilo.

</dd> <dt>

*ppScanProfile* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Indirizzo di un puntatore al profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se un profilo di analisi viene salvato usando il [**metodo Save,**](-wia-iscanprofile-save.md) viene archiviato come file XML in %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

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

 

 





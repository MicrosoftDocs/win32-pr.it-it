---
description: Restituisce il GUID del profilo.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: Metodo IScanProfile::GetGUID (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 37d383d5975957c45b2aa5a0c90350f794e6f20deb9a7bfbe73c9f2d42b2bca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441579"
---
# <a name="iscanprofilegetguid-method"></a>Metodo IScanProfile::GetGUID

Restituisce il GUID del profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*retVal* \[ Cambio\]
</dt> <dd>

Tipo: **\* GUID**

Puntatore al GUID del profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il GUID per un profilo viene generato automaticamente quando il profilo viene creato con [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





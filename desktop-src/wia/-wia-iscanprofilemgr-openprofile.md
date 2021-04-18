---
description: Apre un profilo di analisi salvato su disco come file XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Metodo IScanProfileMgr:: OpenProfile (Scanprofilemgr. h)'
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
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312430"
---
# <a name="iscanprofilemgropenprofile-method"></a>Metodo IScanProfileMgr:: OpenProfile

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

*GUID* \[ in\]
</dt> <dd>

Tipo: **GUID**

GUID del profilo.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Indirizzo di un puntatore al profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se un profilo di analisi viene salvato utilizzando il metodo [**Save**](-wia-iscanprofile-save.md) , viene archiviato come file XML in% UserProfile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





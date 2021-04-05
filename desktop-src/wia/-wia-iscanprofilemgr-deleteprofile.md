---
description: Elimina il profilo di analisi specificato.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Metodo IScanProfileMgr::D eleteProfile (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967574"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr::D Metodo eleteProfile

Elimina il profilo di analisi specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pScanProfile* \[ in\]
</dt> <dd>

Tipo: **[**IScanProfile**](-wia-iscanprofile.md) \** _

Puntatore al profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

**IScanProfileMgr::D eleteprofile** Elimina il profilo dal disco ed Elimina l'oggetto profilo in memoria.

Usare il metodo [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando è possibile che più di un oggetto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) crei o elimini i profili nello stesso momento.

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

 

 





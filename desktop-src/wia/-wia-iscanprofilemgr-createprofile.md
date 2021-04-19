---
description: Crea un profilo di analisi vuoto e lo associa a uno scanner o ad altro elemento Windows Image Acquisition (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Metodo IScanProfileMgr:: CreateProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485293"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>Metodo IScanProfileMgr:: CreateProfile

Crea un profilo di analisi vuoto e lo associa a uno scanner o ad altro elemento Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

ID del dispositivo o dell'elemento WIA 2,0.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Nome descrittivo del nuovo profilo.

</dd> <dt>

*guidCategory* \[ in\]
</dt> <dd>

Tipo: **GUID**

GUID della categoria del dispositivo o dell'elemento WIA 2,0. Deve corrispondere a una delle costanti di \_ categoria degli elementi dell'IPA WIA \_ \_ .

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Indirizzo di un puntatore al nuovo profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

**IScanProfileMgr:: CreateProfile** associa il dispositivo specificato al nuovo profilo di analisi.

**IScanProfileMgr:: CreateProfile** genera automaticamente un GUID per il nuovo profilo. Ottenere il GUID con [**GetGuid**](-wia-iscanprofile-getguid.md).

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

 

 





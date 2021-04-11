---
description: Ottiene il numero di profili di analisi per il dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Metodo IScanProfileMgr:: GetNumProfilesforDeviceID (Scanprofilemgr. h)'
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
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226324"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>Metodo IScanProfileMgr:: GetNumProfilesforDeviceID

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

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

ID del dispositivo.

</dd> <dt>

*pulNumProfiles* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Puntatore al numero di profili disponibili per il dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

 

 





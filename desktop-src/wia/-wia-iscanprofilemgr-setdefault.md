---
description: Imposta il profilo di analisi specificato come profilo predefinito.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Metodo IScanProfileMgr:: IsDefault (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312429"
---
# <a name="iscanprofilemgrsetdefault-method"></a>Metodo IScanProfileMgr:: sedefault

Imposta il profilo di analisi specificato come profilo predefinito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefault(
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

Usare il metodo **IScanProfileMgr:: sedefault** per aggiungere un `<Default>` elemento al profilo o rimuovere tale elemento dal profilo predefinito precedente del dispositivo.

Usare il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) per modificare il profilo predefinito.

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

 

 





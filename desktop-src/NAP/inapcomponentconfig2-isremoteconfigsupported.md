---
title: Metodo INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per indicare se la configurazione remota è supportata.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- NAP metodo IsRemoteConfigSupported
- Metodo IsRemoteConfigSupported NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964015"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>Metodo INapComponentConfig2:: IsRemoteConfigSupported

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **IsRemoteConfigSupported** viene implementato da convalida integrità sistema (SHV) per indicare se la configurazione remota è supportata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*supportato* \[ out\]
</dt> <dd>

Puntatore a un BOOL che è impostato su **true** se il componente supporta la configurazione remota e **false** in caso contrario.

</dd> <dt>

*remoteConfigType* \[ out\]
</dt> <dd>

Indica il tipo di configurazione remota supportato usando il valore dell'enumerazione [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :



| Valore                                                                                                 | Significato                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) è implementato.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) è implementato. [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig:: Seconfig**](inapcomponentconfig-setconfig.md) possono essere chiamati in remoto mediante DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.

## <a name="remarks"></a>Commenti

Se non viene implementato né [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) né [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) , non è possibile configurare in remoto il servizio di convalida dell'integrità di sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 






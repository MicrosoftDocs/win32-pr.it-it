---
title: Metodo INapComponentConfig2 IsRemoteConfigSupported (NapCommon.h)
description: Viene implementato dai validator di integrità del sistema per indicare se la configurazione remota è supportata.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Metodo IsRemoteConfigSupported NAP
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
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621768"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>Metodo INapComponentConfig2::IsRemoteConfigSupported

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo IsRemoteConfigSupported viene** implementato dai validator di integrità del sistema per indicare se la configurazione remota è supportata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isSupported* \[ Cambio\]
</dt> <dd>

Puntatore a un oggetto BOOL impostato su **TRUE** se il componente supporta la configurazione remota e **FALSE** in caso contrario.

</dd> <dt>

*remoteConfigType* \[ Cambio\]
</dt> <dd>

Indica il tipo di configurazione remota supportato usando il valore [**dell'enumerazione RemoteConfigurationType:**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype)



| Valore                                                                                                 | Significato                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) viene implementato.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) è implementato. [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) possono essere chiamati in modalità remota tramite DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o uno dei codici di Windows standard.

## <a name="remarks"></a>Commenti

Se non [**vengono implementati né InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) né [**InvokeUIFromConfigBlob,**](inapcomponentconfig2-invokeuifromconfigblob.md) la configurazione remota di SHV non è possibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 






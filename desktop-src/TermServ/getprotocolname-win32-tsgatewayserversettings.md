---
title: Metodo GetProtocolName della classe Win32_TSGatewayServerSettings
description: Restituisce il nome del protocollo per l'indice del protocollo specificato.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Metodo GetProtocolName Servizi Desktop remoto
- Metodo GetProtocolName Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo , GetProtocolName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b70ee57d8940dc65b1f7b74151a3dd6889286a26e7bbf4357bea4aae8c5259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757823"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo GetProtocolName della classe \_ TSGatewayServerSettings Win32

Restituisce il nome del protocollo per l'indice del protocollo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolId* \[ Pollici\]
</dt> <dd>

Indice dell'identificatore di protocollo. Il valore deve essere compreso tra zero e il valore della **proprietà MaxProtocols.**

</dd> <dt>

*ProtocolName* \[ Cambio\]
</dt> <dd>

Restituisce il nome del protocollo specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

È supportato un protocollo.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


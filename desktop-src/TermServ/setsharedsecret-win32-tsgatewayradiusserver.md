---
title: Metodo SetSharedSecret della Win32_TSGatewayRADIUSServer classe
description: Imposta la proprietà SharedSecret per questo server Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Metodo SetSharedSecret Servizi Desktop remoto
- Metodo SetSharedSecret Servizi Desktop remoto , Win32_TSGatewayRADIUSServer classe
- Win32_TSGatewayRADIUSServer classe Servizi Desktop remoto, metodo SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9d6c37b4826b451a932ff282b451c77aef22c91e92a6c47cd3907ce2705371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008651"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo SetSharedSecret della classe \_ Win32 TSGatewayRADIUSServer

Imposta la **proprietà SharedSecret** per questo server Remote Authentication Dial-In User Service (RADIUS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SharedSecret* \[ Pollici\]
</dt> <dd>

Nuovo segreto condiviso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


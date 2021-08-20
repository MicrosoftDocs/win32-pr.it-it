---
title: Metodo EnableAllowOnlySDRServers della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Usato per attivare o disattivare la proprietà AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Metodo EnableAllowOnlySDRServers Servizi Desktop remoto
- Il metodo EnableAllowOnlySDRServers Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto , metodo EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e2f087b2fbb460093a0ccb623bd89ca7882686be7df516090d443a27a6ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940065"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo EnableAllowOnlySDRServers della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Usato per attivare o **disattivare la proprietà AllowOnlySDRServers.**

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AllowOnlySDRServers* \[ Pollici\]
</dt> <dd>

Se impostato su **True,** le connessioni saranno consentite solo ai server Servizi Desktop remoto di reindirizzamento del dispositivo (SDR). Se impostato su **False,** le connessioni saranno consentite anche ai server Servizi Desktop remoto meno recenti

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | ROOT \\ cimv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TsGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 






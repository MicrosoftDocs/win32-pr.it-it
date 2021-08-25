---
title: Metodo SetSmartcardAllowed della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà SmartcardAllowed, che abilita o disabilita il supporto per l'uso di un smart card per la connessione al server gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Metodo SetSmartcardAllowed Servizi Desktop remoto
- Metodo SetSmartcardAllowed Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto, metodo SetSmartcardAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ea5618bd974c2051a588f532cac9fa741563f6d96be312c50fd9923497d9ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870071"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo SetSmartcardAllowed della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Imposta la **proprietà SmartcardAllowed,** che abilita o disabilita il supporto per l'uso di un smart card per la connessione al server gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Consentito* \[ Pollici\]
</dt> <dd>

Nuovo **valore SmartcardAllowed.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


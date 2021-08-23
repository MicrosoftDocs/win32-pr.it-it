---
title: Metodo EnableOnlyConsentCapableClients della Win32_TSGatewayServerSettings classe
description: Imposta la proprietà OnlyConsentCapableClients.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Metodo EnableOnlyConsentCapableClients Servizi Desktop remoto
- Metodo EnableOnlyConsentCapableClients Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto , metodo EnableOnlyConsentCapableClients
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254eaa15a899eb5612658a4a9ed9b3a7677ca928e202cf5ddebd653d703e31da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059629"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo EnableOnlyConsentCapableClients della classe \_ Win32 TSGatewayServerSettings

Imposta la **proprietà OnlyConsentCapableClients.**

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OnlyConsentCapableClients* \[ Pollici\]
</dt> <dd>

Tipo: **booleano**

Specifica il nuovo valore per la **proprietà OnlyConsentCapableClients.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


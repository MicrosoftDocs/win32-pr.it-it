---
title: Metodo EnableCentralCAP della classe Win32_TSGatewayServerSettings
description: Controlla la proprietà CentralCAPEnabled, che controlla i Servizi Desktop remoto di autorizzazione della connessione (RD \ 160; CAP) per il server Desktop remoto Gateway Desktop remoto.
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Metodo EnableCentralCAP Servizi Desktop remoto
- Metodo EnableCentralCAP Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53bc180d2f4636ed2fd8d7b32d819a9d953416e4022b5cf4c18a900b15776fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574761"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo EnableCentralCAP della classe \_ TSGatewayServerSettings Win32

Controlla la **proprietà CentralCAPEnabled,** che controlla i criteri Servizi Desktop remoto di autorizzazione della connessione desktop remoto per il server gateway Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CentralCAPEnabled* \[ Pollici\]
</dt> <dd>

Se impostato su **True,** verranno usati i criteri di autorizzazione accesso Desktop remoto dai server di Criteri di autorizzazione connessioni Desktop remoto centrali. Se impostato su **False,** verranno usati solo i criteri del server locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 


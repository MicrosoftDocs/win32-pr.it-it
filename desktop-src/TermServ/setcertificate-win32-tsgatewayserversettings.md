---
title: Metodo SetCertificate della classe Win32_TSGatewayServerSettings
description: Imposta l'hash del certificato per l'associazione HTTPS sulla porta 443 in IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- Metodo SetCertificate Servizi Desktop remoto
- Metodo SetCertificate Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo SetCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54b11f87e3cdc8c5c211f67e03a067690ddeac5ab3bc342794e1e97a8f339117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127476"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetCertificate della classe \_ TSGatewayServerSettings Win32

Imposta l'hash del certificato per l'associazione HTTPS sulla porta 443 in IIS.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertHash* \[ Pollici\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Nuovo hash del certificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Dopo aver impostato l'hash del certificato con questo metodo, è necessario chiamare il [**metodo Configure**](configure-win32-tsgatewayserversettings.md) per completare il processo di configurazione.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


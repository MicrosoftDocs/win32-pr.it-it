---
title: Metodo FindLicenseServers della classe Win32_TerminalServiceSetting
description: Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Metodo FindLicenseServers Servizi Desktop remoto
- Metodo FindLicenseServers Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto, metodo FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98af0d63c736e5bc82dd13d2abc94786634d7b92ba2c9a4628ae8ffd32a18b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130790"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a>Metodo FindLicenseServers della classe TerminalServiceSetting Win32 \_

Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServersList* \[ Cambio\]
</dt> <dd>

Elenco di [**oggetti \_ TSDiscoveredLicenseServer Win32.**](win32-tsdiscoveredlicenseserver.md) Ogni oggetto nell'elenco di output ha il nome del server Desktop remoto licenze e il metodo di individuazione.

</dd> <dt>

*Conteggio* \[ Cambio\]
</dt> <dd>

Numero totale di server licenze Desktop remoto individuati nell'elenco di output.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo spazio \\ dei \\ nomi TerminalServices CIMV2 radice, il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **di RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic chiamate di script e script, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 


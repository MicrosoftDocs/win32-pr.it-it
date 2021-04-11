---
title: Metodo FindLicenseServers della classe Win32_TerminalServiceSetting
description: Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FindLicenseServers
- Metodo FindLicenseServers Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo FindLicenseServers
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
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964817"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a>Metodo FindLicenseServers della \_ classe TerminalServiceSetting Win32

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

*LicenseServersList* \[ out\]
</dt> <dd>

Elenco di oggetti [**\_ TSDiscoveredLicenseServer Win32**](win32-tsdiscoveredlicenseserver.md) . Ogni oggetto nell'elenco di output ha il nome del server licenze Desktop remoto e il metodo di individuazione.

</dd> <dt>

*Numero* \[ di out\]
</dt> <dd>

Il numero totale di server licenze Desktop remoto individuati nell'elenco di output.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6. Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


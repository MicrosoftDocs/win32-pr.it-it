---
title: Metodo GetWinstationDriverNames della classe Win32_TerminalServiceSetting
description: Recupera un elenco di nomi di driver Winstation.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Metodo GetWinstationDriverNames Servizi Desktop remoto
- Metodo GetWinstationDriverNames Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo , GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d51d31e6a9857dd1ec1faf46df2adadc4379c0ccf99a7a5ed634a4fa27bf4d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059479"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetWinstationDriverNames della classe TerminalServiceSetting Win32 \_

Recupera un elenco di nomi di driver Winstation.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WinstaDriverNames* \[ Cambio\]
</dt> <dd>

Elenco di nomi di driver Winstation.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo spazio \\ dei \\ nomi TerminalServices CIMV2 radice, il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **di RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 


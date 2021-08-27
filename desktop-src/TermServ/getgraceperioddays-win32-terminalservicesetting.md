---
title: Metodo GetGracePeriodDays della Win32_TerminalServiceSetting classe
description: Recupera il numero di giorni rimanenti nel periodo di tolleranza Servizi Desktop remoto licenze per un server host Desktop remoto sessione Desktop remoto. Un valore zero indica che il periodo di tolleranza è finito.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Metodo GetGracePeriodDays Servizi Desktop remoto
- Metodo GetGracePeriodDays Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto , metodo GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbfe1a99fb0b4f12db19f018d8acb3aaee6ab15a3560cd9140c3a05f36986585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010121"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Metodo GetGracePeriodDays della classe TerminalServiceSetting Win32 \_

Recupera il numero di giorni rimanenti nel periodo di tolleranza Servizi Desktop remoto licenze per un server host Desktop remoto sessione Desktop remoto. Un valore zero indica che il periodo di tolleranza è finito.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DaysLeft* \[ Cambio\]
</dt> <dd>

Numero di giorni rimanenti nel periodo di tolleranza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo spazio \\ dei \\ nomi CIMV2 \\ TerminalServices radice, il livello di autenticazione deve includere la privacy dei pacchetti. Per le chiamate C/C++, questo è un livello di autenticazione di **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32ServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 


---
title: Metodo CanAccessLicenseServer della classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer non è più disponibile.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Metodo CanAccessLicenseServer Servizi Desktop remoto
- Metodo CanAccessLicenseServer Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto metodo , CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0512f42d0d814793f4ecd62fda2dd84005a4183e8db736bd16919799b4570a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139144"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo CanAccessLicenseServer della classe TerminalServiceSetting Win32 \_

\[**CanAccessLicenseServer** non è più disponibile per l'uso a Windows Server 2008 R2.\]

**Windows Server 2008: **

Determina se il server Host sessione Desktop remoto (Host sessione Desktop remoto) è autorizzato a richiedere licenze CAL (Client Access License) Servizi Desktop remoto da un server licenze Desktop remoto in base agli elementi seguenti:

-   L'impostazione di Criteri di gruppo "gruppo di sicurezza del server licenze" nel server Desktop remoto licenze.
-   Appartenenza al gruppo locale Computer Terminal Server nel server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NomeServer* \[ Pollici\]
</dt> <dd>

Nome del server Desktop remoto licenze.

</dd> <dt>

*AccessAllowed* \[ Cambio\]
</dt> <dd>

Indica se al server Host sessione Desktop remoto è consentito richiedere licenze CAL Servizi Desktop remoto dal server licenze.

<dt>

0
</dt> <dd>

La richiesta è consentita.

</dd> <dt>

1
</dt> <dd>

La richiesta non è consentita.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** il server Host sessione Desktop remoto ha accesso al server licenze. Restituisce **S \_ FALSE se** il server Host sessione Desktop remoto non ha accesso al server licenze.

## <a name="remarks"></a>Commenti

L'impostazione dei criteri "Gruppo di sicurezza del server licenze" consente di specificare i server Host sessione Desktop remoto autorizzati a contattare il server licenze per ottenere le licenze CAL Servizi Desktop remoto. Se l'impostazione dei criteri è abilitata nel server licenze, il server licenze risponderà solo alle richieste CAL Servizi Desktop remoto dai server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale Computer Terminal Server nel server licenze.

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
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32ServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 


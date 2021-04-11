---
title: Metodo CanAccessLicenseServer della classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer non è più disponibile.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CanAccessLicenseServer
- Metodo CanAccessLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo CanAccessLicenseServer
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
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119279"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo CanAccessLicenseServer della \_ classe TerminalServiceSetting Win32

\[**CanAccessLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]

* * Windows Server 2008: * *

Determina se il server di host sessione Desktop remoto (host sessione Desktop remoto) può richiedere Servizi Desktop remoto licenze CAL (Client Access License) da un server Desktop remoto License basato sui seguenti elementi:

-   Impostazione dei criteri di gruppo "gruppo di sicurezza del server licenze" nel server licenze Desktop remoto.
-   Appartenenza al gruppo locale computer Terminal Server nel server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nomeserver* \[ in\]
</dt> <dd>

Nome del server licenze Desktop remoto.

</dd> <dt>

*AccessAllowed* \[ out\]
</dt> <dd>

Indica se il server Host sessione Desktop remoto è autorizzato a richiedere licenze CAL Servizi Desktop remoto dal server licenze.

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

Restituisce **\_ OK** se il server Host sessione Desktop remoto ha accesso al server licenze. Restituisce **\_ false** se il server Host sessione Desktop remoto non dispone dell'accesso al server licenze.

## <a name="remarks"></a>Commenti

L'impostazione dei criteri "gruppo di sicurezza del server licenze" consente di specificare i server Host sessione Desktop remoto autorizzati a contattare il server licenze per ottenere le licenze CAL Servizi Desktop remoto. Se l'impostazione dei criteri è abilitata nel server licenze, il server licenze risponderà solo alle richieste CAL Servizi Desktop remoto dei server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale computer Terminal Server nel server licenze.

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
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


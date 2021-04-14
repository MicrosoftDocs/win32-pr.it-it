---
title: Classe Win32_TSDiscoveredLicenseServer
description: Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSDiscoveredLicenseServer Servizi Desktop remoto
- Classe Win32_TSDiscoveredLicenseServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478826"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a>Win32 \_ TSDiscoveredLicenseServer (classe)

Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSDiscoveredLicenseServer** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSDiscoveredLicenseServer** dispone di queste proprietà.

<dl> <dt>

**HowDiscovered**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è più supportata.

**Windows Server 2008:** Metodo di individuazione del server licenze Desktop remoto.

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)


</dt> <dd>

Il server licenze è stato individuato tramite criteri di gruppo.

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)


</dt> <dd>

Il server licenze è stato individuato tramite un'impostazione del registro di sistema.

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)


</dt> <dd>

Il server licenze è stato individuato utilizzando l'ambito di individuazione del gruppo di lavoro.

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)


</dt> <dd>

Il server licenze è stato individuato utilizzando l'ambito di individuazione dominio.

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)


</dt> <dd>

Il server licenze è stato individuato utilizzando l'ambito di individuazione foresta.

</dd> </dl>

</dd> <dt>

**IsAdminOnLS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'account utilizzato per eseguire lo script o il file exe che utilizza la classe **Win32 \_ TSDiscoveredLicenseServer** dispone dell'accesso di amministratore al server licenze.

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)


</dt> <dd>

L'account utilizzato non dispone dell'accesso di amministratore al server licenze.

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Sì** (1)


</dt> <dd>

L'account utilizzato dispone di accesso amministrativo al server licenze.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Non **so** (2)


</dt> <dd>

Non è possibile determinare se l'account utilizzato dispone di accesso amministrativo al server licenze.

</dd> </dl>

</dd> <dt>

**IsLSAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il server licenze è disponibile, ovvero se è possibile stabilire \[ una \] connessione RPC al server.

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)


</dt> <dd>

Il server licenze non è disponibile.

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (1)


</dt> <dd>

Il server licenze è disponibile.

</dd> </dl>

</dd> <dt>

**IssuingCALs**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il server licenze è autorizzato a emettere le licenze CAL (Client Access License) di Servizi Desktop remoto al server Host sessione Desktop remoto.

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non consentito** (0)


</dt> <dd>

Il server licenze non è autorizzato ad emettere licenze CAL Servizi Desktop remoto per il server Host sessione Desktop remoto.

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Consentito** (1)


</dt> <dd>

Il server licenze può emettere licenze CAL Servizi Desktop remoto per il server Host sessione Desktop remoto.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Non **so** (2)


</dt> <dd>

Non è possibile determinare se il server licenze è autorizzato a rilasciare licenze CAL Servizi Desktop remoto al server Host sessione Desktop remoto.

</dd> </dl>

</dd> <dt>

**LicenseServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server licenze Desktop remoto individuato.

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
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 


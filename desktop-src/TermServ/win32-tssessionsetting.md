---
title: Classe Win32_TSSessionSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32, ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSessionSetting Servizi Desktop remoto
- Classe Win32_TSSessionSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518976"
---
# <a name="win32_tssessionsetting-class"></a>Win32 \_ TSSessionSetting (classe)

La classe WMI **Win32 \_ TSSessionSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , ad esempio i limiti di tempo e le azioni di disconnessione e riconnessione.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSSessionSetting** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSSessionSetting** presenta questi metodi.



| Metodo                                                              | Descrizione                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**BrokenConnection**](win32-tssessionsetting-brokenconnection.md) | Imposta le proprietà di connessione interrotte incluse in questa classe.<br/> |
| [**Limite**](win32-tssessionsetting-timelimit.md)               | Imposta le proprietà del limite di tempo incluse in questa classe.<br/>        |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSSessionSetting** dispone di queste proprietà.

<dl> <dt>

**ActiveSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità massima di tempo, in millisecondi, allocata a una sessione attiva. Il valore 0 specifica un periodo di tempo infinito.

</dd> <dt>

**BrokenConnectionAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione eseguita dal server in caso di interruzione di una connessione a causa della perdita di rete o del superamento dei limiti di tempo.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnetti** (0)


</dt> <dd>

L'utente è disconnesso dalla sessione.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (1)


</dt> <dd>

La sessione viene eliminata definitivamente dal server.

</dd> </dl>

</dd> <dt>

**BrokenConnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il criterio utilizzato dal server per determinare quando interrompere una connessione a causa di una perdita di rete o di limiti di tempo superati.

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)


</dt> <dd>

Le impostazioni dei criteri di disconnessione dell'utente vengono sostituite dal server.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)


</dt> <dd>

Le impostazioni dei criteri di disconnessione dell'utente sono attive.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa a una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo, in millisecondi, dopo il quale una sessione disconnessa viene terminata. Il valore 0 specifica un periodo di tempo infinito.

</dd> <dt>

**EnableTimeoutWarning**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Consente di abilitare l'avviso di timeout.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**IdleSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo, in millisecondi, dopo il quale una sessione inattiva viene terminata. Il valore 0 specifica un periodo di tempo infinito.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceActiveSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ActiveSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceBrokenConnectionAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **BrokenConnectionAction** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceDisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **DisconnectedSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceIdleSessionLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **IdleSessionLimit** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceReconnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ReconnectPolicy** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**ReconnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se un utente deve utilizzare il client precedente per riconnettersi a una sessione disconnessa.

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Qualsiasi client** (0)


</dt> <dd>

Qualsiasi client verrà usato per la riconnessione.

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Client precedente** (1)


</dt> <dd>

Il client precedente utilizzato in una connessione verrà utilizzato per la riconnessione.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Errore")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Errore di predazione")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminale**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**TimeLimitPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il criterio utilizzato dal server per determinare i limiti di tempo per le sessioni utente.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)


</dt> <dd>

Sono attive le impostazioni dei criteri per i limiti di tempo dell'utente.

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Sostituzione server** (1)


</dt> <dd>

Le impostazioni dei criteri per i limiti di tempo dell'utente vengono sostituite dal server.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che WinStations associato alla sessione della console non può accedere ai metodi e alle proprietà di questa classe. Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**. Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto allo scopo di aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.

Per connettersi allo \\ \\ spazio dei nomi "root cimv2 TerminalServices", il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6. Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


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

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dt>

[**\_Impostazione CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 


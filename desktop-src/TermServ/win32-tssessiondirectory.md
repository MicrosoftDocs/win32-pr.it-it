---
title: Classe Win32_TSSessionDirectory
description: Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la \_ classe Win32 TSSessionDirectorySetting.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSessionDirectory Servizi Desktop remoto
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964072"
---
# <a name="win32_tssessiondirectory-class"></a>Win32 \_ TSSessionDirectory (classe)

Definisce le impostazioni di configurazione di Connessione Desktop remoto broker (gestore connessione Desktop remoto) per la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

> [!Note]  
> In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto. Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.

 

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSSessionDirectory** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSSessionDirectory** presenta questi metodi.



| Metodo                                                                                                  | Descrizione                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**CreateUserDiskTemplate**](createuserdisktemplate-win32-tssessiondirectory.md)                       | Crea un modello di disco utente.<br/>                                                                     |
| [**DisableUserVhd**](disableuservhd-win32-tssessiondirectory.md)                                       | Disabilita un disco rigido virtuale del profilo utente.<br/>                                                                      |
| [**EnableUserVhd**](enableuservhd-win32-tssessiondirectory.md)                                         | Abilita un VHD del profilo utente in un server RDSH.<br/>                                                     |
| [**GetCurrentRedirectableAddresses**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Ottiene l'elenco attualmente configurato di indirizzi DNS idonei e il tipo di reindirizzamento.<br/>        |
| [**GetRedirectableAddresses**](getredirectableaddresses-win32-tssessiondirectory.md)                   | Ottiene l'intero elenco di indirizzi DNS idonei.<br/>                                                |
| [**PingSessionDirectory**](pingsessiondirectory-win32-tssessiondirectory.md)                           | Verifica se il server Gestore connessione Desktop remoto è disponibile.<br/>                                      |
| [**SetCurrentRedirectableAddresses**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Imposta l'elenco configurato di indirizzi DNS idonei e il tipo di reindirizzamento.<br/>                     |
| [**SetLoadBalancingState**](setloadbalancingstate-win32-tssessiondirectory.md)                         | Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.<br/> |
| [**SetServerWeight**](setserverweight-win32-tssessiondirectory.md)                                     | Imposta il valore del peso del server per il bilanciamento del carico di gestore connessione Desktop remoto.<br/>                             |
| [**SetSessionDirectoryActive**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | Disabilita e Abilita il gestore connessione Desktop remoto.<br/>                                                    |
| [**SetSessionDirectoryExposeServerIP**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | Imposta la proprietà **SessionDirectoryExposeServerIP** .<br/>                                             |
| [**SetSessionDirectoryProperty**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | Imposta la proprietà **SessionDirectoryLocation** o la proprietà **SessionDirectoryClusterName** .<br/>   |
| [**SetTSRedirectorMode**](settsredirectormode-win32-tssessiondirectory.md)                             | Questo metodo non è disponibile.<br/>                                                                     |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSSessionDirectory** dispone di queste proprietà.

<dl> <dt>

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

**GetLoadBalancingState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il server è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

Il server non è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Il server è configurato per partecipare al bilanciamento del carico di gestore connessione Desktop remoto.

</dd> </dl>

</dd> <dt>

**GetServerWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Recupera il valore del peso del server utilizzato nel bilanciamento del carico di gestore connessione Desktop remoto.

</dd> <dt>

**GetTSRedirectorMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il server è configurato per fungere da redirector Servizi Desktop remoto.

<dt>

0
</dt> <dd>

Il server è configurato per fungere da redirector Servizi Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Il server non è configurato per fungere da redirector Servizi Desktop remoto.

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile.

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

**PolicySourceLoadBalancing**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **GetLoadBalancingState** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryActive**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SessionDirectoryActive** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SessionDirectoryClusterName** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SessionDirectoryExposeServerIP** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SessionDirectoryLocation** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceTSRedirectorMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è disponibile.

**Windows Server 2008 R2:** Indica se la proprietà **GetTSRedirectorMode** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**SessionDirectoryActive**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Specifica se Servizi Desktop remoto partecipa al gestore connessione Desktop remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Servizi Desktop remoto partecipazione al gestore connessione Desktop remoto è disabilitata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Servizi Desktop remoto la partecipazione al gestore connessione Desktop remoto è abilitata.

</dd> </dl>

</dd> <dt>

**SessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo IP virtuale del cluster a cui appartiene il server Host sessione Desktop remoto.

</dd> <dt>

**SessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se è consentito il recupero dell'indirizzo IP del gestore connessione Desktop remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Recupero negato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il recupero è consentito.

</dd> </dl>

</dd> <dt>

**SessionDirectoryIPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indirizzo IP della scheda LAN utilizzata dalla directory di sessione.

</dd> <dt>

**SessionDirectoryLocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome DNS di rete o indirizzo IP del server in cui è in esecuzione il servizio Gestore connessione Desktop remoto.

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

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo \\ \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.

Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



In Windows Server 2008, il nome della funzionalità directory di sessione di Servizi terminal è stato modificato in Gestore sessioni Servizi terminal.

In Windows Server 2008 R2 il nome della funzionalità gestore sessioni Servizi terminal è stato modificato in Connessione Desktop remoto broker.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[**\_TSSessionDirectorySetting Win32**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 


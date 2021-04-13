---
description: Win32 \_ NetworkProtocol&\# 8194; La classe WMI rappresenta un protocollo e le relative caratteristiche di rete in un computer Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483789"
---
# <a name="win32_networkprotocol-class"></a>Win32 \_ NetworkProtocol (classe)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol Win32** rappresenta un protocollo e le relative caratteristiche di rete in un computer Win32.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ NetworkProtocol** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ NetworkProtocol** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConnectionlessService**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags XP1 senza \| \_ connessione")
</dt> </dl>

Il protocollo supporta il servizio senza connessione. Un servizio senza connessione (datagramma) descrive un protocollo di comunicazione o un trasporto in cui i pacchetti di dati vengono instradati in modo indipendente l'uno dall'altro e possono seguire diverse route e arrivare in un ordine diverso rispetto a quello in cui sono stati inviati. Viceversa, un servizio orientato alla connessione fornisce un circuito virtuale attraverso il quale i pacchetti di dati vengono ricevuti nello stesso ordine in cui sono stati trasmessi. Se la connessione tra computer ha esito negativo, l'applicazione riceve una notifica.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ \_ recapito garantito")
</dt> </dl>

Il protocollo supporta la distribuzione di pacchetti di dati. Se questo flag è **false**, non è certo che tutti i dati inviati raggiungano la destinazione prevista.

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags XP- \| \_ \_ ordine garantito")
</dt> </dl>

Il protocollo garantisce che i dati arrivino nell'ordine in cui sono stati inviati. Tenere presente che questa caratteristica non garantisce il recapito dei dati, ma solo il relativo ordine.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| iMaxSockAddr"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")
</dt> </dl>

Lunghezza massima di un indirizzo socket supportato dal protocollo. Gli indirizzi socket possono essere elementi come un URL ( `www.microsoft.com` ) o un indirizzo IP ( `130.215.24.1` ).

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| dwMessageSize"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")
</dt> </dl>

Dimensione massima del messaggio supportata dal protocollo. Dimensione massima di un messaggio che può essere inviato o ricevuto dall'host. Per i protocolli che non supportano il framing dei messaggi, la dimensione massima effettiva di un messaggio che può essere inviato a un indirizzo specificato potrebbe essere minore di questo valore.

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures ( \| informazioni sul protocollo \_ \| \| ) dwServiceFlags XP \_ message \_ oriented")
</dt> </dl>

Il protocollo è orientato ai messaggi. Un protocollo orientato ai messaggi utilizza pacchetti di dati per trasferire le informazioni. Viceversa, i protocolli orientati al flusso trasferiscono i dati come flusso continuo di byte.

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| iMinSockAddr"), [**unità**](../wmisdk/standard-qualifiers.md) ("caratteri")
</dt> </dl>

Lunghezza minima di un indirizzo socket supportato dal protocollo.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("nome"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocol \_ info \| lpProtocol")
</dt> </dl>

Nome del protocollo.

Esempio: "TCP/IP"

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ pseudo \_ Stream")
</dt> </dl>

Il protocollo è un protocollo orientato ai messaggi che può ricevere pacchetti di dati a lunghezza variabile o dati trasmessi per tutte le operazioni di ricezione. Questa funzionalità facoltativa è utile quando un'applicazione non vuole che il protocollo consenta di incorniciare i messaggi e richiede caratteristiche orientate al flusso. Se **true**, il protocollo è pseudo-orientato al flusso.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto. È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "danneggiato" e "errore predazione". "Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "starting", "stoping" e "Service". Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures, \| informazioni sul protocollo \_ \| dwServiceFlags \| XP supporta la \_ \_ trasmissione")
</dt> </dl>

Il protocollo supporta un meccanismo per la trasmissione di messaggi attraverso la rete.

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures ( \| informazioni sul protocollo \_ \| \| ) dwServiceFlags XP \_ Connect \_ Data")
</dt> </dl>

Il protocollo consente la connessione dei dati attraverso la rete.

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Disconnetti \_ dati")
</dt> </dl>

Il protocollo consente la disconnessione dei dati attraverso la rete.

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Encrypts")
</dt> </dl>

Il protocollo supporta la crittografia dei dati.

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ Accelerated \_ Data")
</dt> </dl>

Il protocollo supporta dati accelerati (noti anche come dati urgenti) attraverso la rete. I dati accelerati possono ignorare il controllo di flusso e ricevere la priorità rispetto ai pacchetti di dati normali.

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures Structures \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ frammentazione")
</dt> </dl>

Il protocollo supporta la trasmissione dei dati in frammenti. L'unità di trasferimento massima (MTU) della rete fisica è nascosta per le applicazioni. Ogni tipo di supporto ha una dimensione massima del frame che non può essere superata. Il livello di collegamento individua il MTU e lo segnala ai protocolli utilizzati.

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ normale \_ Close")
</dt> </dl>

Il protocollo supporta operazioni di chiusura in due fasi, note anche come "operazioni di chiusura normali". In caso contrario, il protocollo supporta solo operazioni di chiusura interrotte.

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures le \| informazioni sul protocollo \_ \| dwServiceFlags \| XP \_ allocazione della larghezza di banda \_ ")
</dt> </dl>

Il protocollo dispone di un meccanismo per stabilire e mantenere una larghezza di banda.

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures, \| informazioni sul protocollo \_ \| dwServiceFlags \| XP supporta il \_ \_ multicast")
</dt> </dl>

Il protocollo supporta il multicast.

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ supported")
</dt> </dl>

Il protocollo è in grado di supportare qualità del servizio (QoS) dal provider di servizi o dal gestore di trasporto sovrapposto sottostante. QoS è una raccolta di componenti che consentono la differenziazione e il trattamento preferenziale per subset di dati trasmessi in rete. QoS significa che i subset di dati ottengono una priorità maggiore o un servizio garantito quando attraversano una rete.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ NetworkProtocol** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze di **Win32 \_ NetworkProtocol**.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



Nell'esempio di codice Perl seguente viene illustrato come recuperare un elenco di servizi in esecuzione da istanze di **Win32 \_ NetworkProtocol**.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LogicalElement CIM**](cim-logicalelement.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 

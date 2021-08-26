---
description: Win32 \_ TCPIPPrinterPort&\# 32; La classe WMI rappresenta un punto di accesso del servizio TCP/IP.
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2861d12740f894cc17a91d6a3f4c2b6792d38f658063bc89474f3656a74b45f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917411"
---
# <a name="win32_tcpipprinterport-class"></a>Classe \_ WIN32 TCPIPPrinterPort

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 TCPIPPrinterPort** rappresenta un punto di accesso al servizio TCP/IP.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a>Members

La **classe \_ WIN32 TCPIPPrinterPort** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WIN32 TCPIPPrinterPort** ha queste proprietà.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il computer conta i byte in un documento prima di inviarli alla stampante e la stampante restituisce il numero di byte effettivamente letti. Questa funzionalità viene usata per la diagnostica quando vengono rilevati byte mancanti nell'output di stampa.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della classe o sottoclasse utilizzata nella creazione di un'istanza di . Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze della classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**HostAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo o del server di stampa.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identifica in modo univoco il punto di accesso del servizio e fornisce un'indicazione della funzionalità gestita. Questa funzionalità è descritta in modo più dettagliato nella proprietà Description dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Portnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porte TCP usate dal monitoraggio delle porte per comunicare con il dispositivo.

</dd> <dt>

**Protocollo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di stampa utilizzato. Alcune stampanti supportano solo la funzionalità LPR.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

RAW

Stampa diretta in un dispositivo o in un server di stampa.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Lpr

Protocollo legacy, che alla fine viene sostituito da RAW.

</dd> </dl>

</dd> <dt>

**Coda**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della coda di stampa nel server quando viene utilizzata con il protocollo LPR.

</dd> <dt>

**SNMPCommunity**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore del livello di sicurezza per il dispositivo.

Esempio: "public'"

</dd> <dt>

**SNMPDevIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di indice SNMP del dispositivo per l'agente SNMP.

</dd> <dt>

**SNMPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** questa stampante supporta [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Simple Network Management Protocol) e può fornire informazioni dettagliate sullo stato dal dispositivo.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto . È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "Danneggiato" e "Pred Fail". "Pred Fail" indica che un elemento funziona correttamente, ma prevede un errore , ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "Starting", "Stopping" e "Service". Il "servizio" può essere applicato durante il ridimensionamento del mirror del disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**SISTEMA CIM \_**](cim-system.md).**CreationClassName**"), [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della classe di creazione del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**SISTEMA CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome del sistema di ambito.

Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Tipo di SAP, ad esempio collegato o reindirizzato.

Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](cim-serviceaccesspoint.md)

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Scrittura** (1)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lettura** (2)


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

**Reindirizzato** (4)


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

**Rete \_ Collegato** (8)


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**sconosciuto** (16)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ TCPIPPrinterPort Win32** deriva da [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) che deriva da [**CIM \_ LogicalElement.**](cim-logicalelement.md)

Il **privilegio SeLoadDriverPrivilege** è necessario per eliminare un'istanza di questa classe WMI. Il frammento di script seguente illustra come stabilire una connessione a WMI che usa questo privilegio.

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a>Esempio

L'esempio di PowerShell seguente rimuove una stampante e la porta della stampante TCPIP associata.


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 

---
description: Rappresenta gli attributi e i comportamenti di una scheda di rete. Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendenti dalla scheda di rete.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153574"
---
# <a name="win32_networkadapterconfiguration-class"></a>Classe NetworkAdapterConfiguration Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapterConfiguration** rappresenta gli attributi e i comportamenti di una scheda di rete. Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendenti dalla scheda di rete.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a>Members

La **classe \_ NetworkAdapterConfiguration Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ NetworkAdapterConfiguration Win32** include questi metodi.



| Metodo                                                                                                                       | Descrizione                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Disabilita IPsec su questa scheda di rete abilitata per TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Abilita il Dynamic Host Configuration Protocol (DHCP) per il servizio con questa scheda di rete.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Abilita il Domain Name System (DNS) per il servizio in questa scheda di rete associata a TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Abilita IPsec a livello globale in tutte le schede di rete associate a IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Abilita IPsec su questa scheda di rete specifica abilitata per TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Abilita l'indirizzamento TCP/IP statico per la scheda di rete di destinazione.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Abilita le impostazioni WINS specifiche di TCP/IP, ma indipendenti dalla scheda di rete.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Rilascia l'indirizzo IP associato a una scheda di rete abilitata per DHCP specifica.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Rilascia gli indirizzi IP associati a tutte le schede di rete abilitate per DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Rinnova l'indirizzo IP su schede di rete abilitate per DHCP specifiche.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Rinnova gli indirizzi IP in tutte le schede di rete abilitate per DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta la trasmissione delle query ARP tramite TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Consente ai pacchetti Ethernet di usare la codifica SNAP 802.3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Imposta il percorso dei file di database Internet standard (HOSTS, LMHOSTS, NETWORKS e PROTOCOLS).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Abilita il rilevamento di gateway non attiva.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsoleta. Questo metodo imposta il valore toS (Type of Service) predefinito nell'intestazione dei pacchetti IP in uscita.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Imposta il valore TTL (Time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Imposta il dominio DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta l'ordine di ricerca del server come matrice di elementi.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta l'ordine di ricerca dei suffissi come matrice di elementi.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indica la registrazione DNS dinamica degli indirizzi IP per questa scheda associata a IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Specifica la quantità di memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda di pacchetti del router.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Specifica un elenco di gateway per il routing di pacchetti destinati a una subnet diversa da quella a cui è connessa la scheda.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Imposta la misura in cui il sistema supporta il multicast IP e partecipa al Internet Group Management Protocol.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Imposta la metrica di routing associata a questa scheda associata a IP.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Imposta l'utilizzo della trasmissione IP zero.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Imposta coppie numero/frame di rete IPX (Internetworking Packet Exchange) per questa scheda di rete.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta l'intervallo che separa le ritrasmissioni Keep-Alive fino alla ricezione di una risposta.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Imposta la frequenza con cui TCP tenta di verificare che una connessione inattiva sia ancora disponibile inviando un pacchetto Keep-Alive.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Imposta l'unità massima di trasmissione (MTU) predefinita per un'interfaccia di rete.<br/> Questo metodo non è supportato.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta il numero di intestazioni di pacchetti IP allocate per la coda di pacchetti del router.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Abilita il rilevamento dei router Black Hole.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Abilita l'individuazione dell'unità massima di trasmissione (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Imposta l'operazione predefinita di NetBIOS su TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Imposta il numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima dell'interruzione.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Imposta il numero di volte in cui TCP ritrasmetterà un singolo segmento di dati prima di interrompere la connessione.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta il numero massimo di connessioni che TCP può avere aperto contemporaneamente.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Specifica se TCP usa la specifica RFC 1122 per i dati urgenti o la modalità usata dai sistemi derivati da Berkeley Software Design (BSD).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Imposta le dimensioni massime della finestra di ricezione TCP offerte dal sistema.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Imposta i server WINS (Windows Internet Naming Service) primari e secondari su questa scheda di rete associata a TCP/IP.<br/>                        |



 

### <a name="properties"></a>Proprietà

La **classe \_ NetworkAdapterConfiguration Win32** ha queste proprietà.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpAlwaysSourceRoute")
</dt> </dl>

Se **TRUE,** TCP/IP trasmette query ARP (Address Resolution Protocol) con routing di origine abilitato nelle reti Token Ring. Per impostazione predefinita (FALSE), ARP esegue prima query senza routing di origine e quindi riprova con il routing di origine abilitato se non viene ricevuta alcuna risposta. Il routing di origine consente il routing dei pacchetti di rete tra diversi tipi di reti.

</dd> <dt>

**ArpUseetherSNAP**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ArpUseEtherSNAP")
</dt> </dl>

Se **TRUE,** i pacchetti Ethernet seguono la codifica SNAP (Sub-Network Access Protocol) IEEE 802.3. L'impostazione di questo parametro su 1 impone a TCP/IP di trasmettere pacchetti Ethernet usando la codifica SNAP 802.3. Per impostazione predefinita (FALSE), lo stack trasmette i pacchetti in formato DIX Ethernet.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**Databasepath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DatabasePath")
</dt> </dl>

Percorso di file windows valido per i file di database Internet standard (HOSTS, LMHOSTS, NETWORKS e PROTOCOLS). Il percorso del file viene usato dall'interfaccia di Windows Sockets.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services Parametri \\ \\ Tcpip \\ \\ \| EnableDeadGWDetect")
</dt> </dl>

Se **TRUE,** viene eseguito il rilevamento di gateway non in tempo reale. Con questa funzionalità abilitata, Transmission Control Protocol (TCP) chiede al protocollo IP (Internet Protocol) di passare a un gateway di backup se ritrasmette un segmento più volte senza ricevere una risposta.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| DefaultGateway")
</dt> </dl>

Matrice di indirizzi IP dei gateway predefiniti utilizzati dal sistema del computer.

Esempio: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTOS")
</dt> </dl>

Valore TOS (Type Of Service) predefinito impostato nell'intestazione dei pacchetti IP in uscita. Request for Comments (RFC) 791 definisce i valori. Valore predefinito: 0 (zero), Intervallo valido: 0 - 255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| DefaultTTL")
</dt> </dl>

Valore TTL (Time To Live) predefinito impostato nell'intestazione dei pacchetti IP in uscita. Il TTL specifica il numero di router che un pacchetto IP può passare per raggiungere la destinazione prima di essere eliminato. Ogni router decrementa di uno il conteggio TTL di un pacchetto durante il passaggio e rimuove i pacchetti, se il valore TTL è 0 (zero). Valore predefinito: 32, Intervallo valido: 1 - 255.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Se **TRUE,** il server DHCP (Dynamic Host Configuration Protocol) assegna automaticamente un indirizzo IP al sistema del computer quando stabilisce una connessione di rete.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Data e ora di scadenza di un indirizzo IP con lease assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).

Esempio: 20521201000230.0000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Data e ora in cui il lease è stato ottenuto per l'indirizzo IP assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).

Esempio: 19521201000230.0000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

Indirizzo IP del server DHCP (Dynamic Host Configuration Protocol).

Esempio: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| Domain")
</dt> </dl>

Nome dell'organizzazione seguito da un punto e da un'estensione che indica il tipo di organizzazione, ad esempio "microsoft.com". Il nome può essere qualsiasi combinazione delle lettere da A a Z, dai numerali da 0 a 9 e dal trattino (-) e dal punto (.) usato come separatore.

Esempio: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| SearchList")
</dt> </dl>

Matrice di suffissi di dominio DNS da aggiungere alla fine dei nomi host durante la risoluzione dei nomi. Quando si tenta di risolvere un nome di dominio completo (FQDN) da un nome solo host, il sistema aggiungerà prima il nome di dominio locale. In caso contrario, il sistema userà l'elenco di suffissi di dominio per creare fqdn aggiuntivi nell'ordine elencato ed eseguire query sui server DNS per ognuno.

Esempio: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnableDNS")
</dt> </dl>

Se **TRUE,** la Domain Name System (DNS) è abilitata per la risoluzione dei nomi su Windows Internet Naming Service (WINS). Se il nome non può essere risolto tramite DNS, la richiesta di nome viene inoltrata a WINS per la risoluzione.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| Hostname")
</dt> </dl>

Nome host usato per identificare il computer locale per l'autenticazione da parte di alcune utilità. Altre utilità basate su TCP/IP possono usare questo valore per acquisire il nome del computer locale. I nomi host vengono archiviati nei server DNS in una tabella che esegue il mapping dei nomi agli indirizzi IP per l'uso da parte del DNS. Il nome può essere qualsiasi combinazione di lettere da A a Z, numeri da 0 a 9 e trattino (-) più il carattere punto (.) usato come separatore. Per impostazione predefinita, questo valore è il nome del computer di rete Microsoft, ma l'amministratore di rete può assegnare un altro nome host senza influire sul nome del computer.

Esempio: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NameServer")
</dt> </dl>

Matrice di indirizzi IP del server da usare per l'esecuzione di query per i server DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** gli indirizzi IP per questa connessione vengono registrati in DNS con il nome di dominio di questa connessione oltre a essere registrati con il nome DNS completo del computer. Il nome di dominio di questa connessione viene impostato usando il [**metodo SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o assegnato da DSCP. Il nome registrato è il nome host del computer con il nome di dominio aggiunto.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ Tcpip Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Memoria allocata da IP per archiviare i dati dei pacchetti nella coda di pacchetti del router. Quando questo spazio del buffer viene riempito, il router inizia a rimuovere i pacchetti in modo casuale dalla coda. I buffer dei dati della coda di pacchetti hanno una lunghezza di 256 byte, quindi il valore di questo parametro deve essere un multiplo di 256. Più buffer vengono concatenati per pacchetti di dimensioni maggiori. L'intestazione IP per un pacchetto viene archiviata separatamente. Questo parametro viene ignorato e non vengono allocati buffer se il router IP non è abilitato. Le dimensioni del buffer possono variare dall'MTU di rete a un valore inferiore a 0xFFFFFFFF. Impostazione predefinita: 74240 (50 pacchetti da 1480 byte, arrotondati a un multiplo di 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** gli indirizzi IP per questa connessione vengono registrati in DNS con il nome DNS completo del computer. Il nome DNS completo del computer viene visualizzato nella scheda **Identificazione** di rete dell'applicazione Sistema in Pannello di controllo.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di valori di metrica dei costi interi (compresi tra 1 e 9999) da usare per calcolare le route più veloci, affidabili o meno a elevato utilizzo di risorse. Questo argomento ha una corrispondenza uno-a-uno con la **proprietà DefaultIPGateway.**

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IGMPLevel")
</dt> </dl>

Misura in cui il sistema supporta il multicast IP e partecipa al Internet Group Management Protocol (IGMP). Al livello 0 (zero), il sistema non fornisce supporto multicast. Al livello 1, il sistema può inviare solo pacchetti multicast IP. Al livello 2, il sistema può inviare pacchetti multicast IP e partecipare completamente a IGMP per ricevere pacchetti multicast.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Nessun multicast** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multicast IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Ip & multicast IGMP** (2)


</dt> <dd>

Ip e multicast IGMP (impostazione predefinita)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet Control Class \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Numero di indice della configurazione della scheda di rete di Windows. Il numero di indice viene usato quando sono disponibili più configurazioni.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di indice che identifica in modo univoco un'interfaccia di rete locale. Il valore di questa proprietà corrisponde al valore della proprietà **InterfaceIndex** nell'istanza di [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) che rappresenta l'interfaccia di rete nella tabella di route.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip \| IPAddress")
</dt> </dl>

Matrice di tutti gli indirizzi IP associati alla scheda di rete corrente. Questa proprietà può contenere indirizzi IPv6 o indirizzi IPv4. Per altre informazioni, vedere [Supporto di IPv6 e IPv4 in WMI.](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)

Indirizzo IPv6 di esempio: "2010:836B:4179::836B:4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Costo dell'uso delle route configurate per la scheda associata IP ed è il valore ponderato per tali route nella tabella di routing IP. Se sono presenti più route per una destinazione nella tabella di routing IP, viene usata la route con la metrica più bassa. Il valore predefinito è 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip")
</dt> </dl>

Se **TRUE,** TCP/IP è associato e abilitato su questa scheda di rete.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| IPFilterSecurityEnabled")
</dt> </dl>

Se **TRUE,** la sicurezza delle porte IP è abilitata a livello globale in tutte le schede di rete associate a IP e i valori di sicurezza associati alle singole schede di rete sono attivati. Questa proprietà viene utilizzata insieme a **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**. Se **FALSE,** la sicurezza del filtro IP è disabilitata in tutte le schede di rete e consente a tutto il traffico di porta e protocollo di fluire senza filtri.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Se **TRUE,** la sicurezza delle porte IP è abilitata a livello globale in tutte le schede di rete associate a IP. Questa proprietà è obsoleta. Al posto di questa proprietà, è necessario usare **IPFilterSecurityEnabled**.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| RawIPAllowedProtocols")
</dt> </dl>

Matrice dei protocolli consentiti per l'esecuzione sull'indirizzo IP. L'elenco di protocolli viene definito usando il [**metodo EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) L'elenco sarà vuoto o conterrà valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutti i protocolli. Una stringa vuota indica che non è consentita l'esecuzione di protocolli **quando IPFilterSecurityEnabled** è **TRUE.**

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TCPAllowedPorts")
</dt> </dl>

Matrice delle porte a cui verrà concessa l'autorizzazione di accesso per TCP. L'elenco dei protocolli viene definito usando [**il metodo EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) L'elenco sarà vuoto o conterrà valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte. Una stringa vuota indica che a nessuna porta viene concessa l'autorizzazione di accesso **quando IPFilterSecurityEnabled** è **TRUE.**

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UDPAllowedPorts")
</dt> </dl>

Matrice delle porte a cui verrà concessa l'autorizzazione di accesso UDP (User Datagram Protocol). L'elenco dei protocolli viene definito usando [**il metodo EnableIPSec.**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) L'elenco sarà vuoto o conterrà valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte. Una stringa vuota indica che a nessuna porta viene concessa l'autorizzazione di accesso **quando IPFilterSecurityEnabled** è **TRUE.**

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| SubnetMask")
</dt> </dl>

Matrice di tutte le subnet mask associate alla scheda di rete corrente.

Esempio: "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| UseZeroBroadcast")
</dt> </dl>

Se **TRUE,** vengono usati ip zeros-broadcast (0.0.0.0) e il sistema usa le trasmissioni uno (255.255.255.255. 255). I sistemi informatici usano in genere le trasmissioni a uno, ma quelle derivate dalle implementazioni di BSD usano le trasmissioni azzeramento. I sistemi che non usano le stesse trasmissioni non interoperativizzano nella stessa rete. Il valore predefinito è **FALSE.**

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets versione 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")
</dt> </dl>

La tecnologia IPX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La tecnologia IPX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| PktType")
</dt> </dl>

La tecnologia IPX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**SNAP Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| MediaType")
</dt> </dl>

La tecnologia IpX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| NetworkNumber")
</dt> </dl>

La tecnologia IPX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DEPRECATO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| VirtualNetworkNumber")
</dt> </dl>

La tecnologia IPX (Internetwork Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Intervallo che separa le ritrasmissioni Keep Alive fino a quando non viene ricevuta una risposta. Dopo la ricezione di una risposta, il ritardo fino alla successiva trasmissione Keep Alive viene nuovamente controllato dal valore **di KeepAliveTime**. La connessione verrà interrotta dopo che il numero di ritrasmissioni specificato da **TcpMaxDataRetransmissions** è stato annullato. Valore predefinito: 1000, Intervallo valido: 1 - 0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

La **proprietà KeepAliveTime** indica la frequenza con cui tcp tenta di verificare che una connessione inattiva sia ancora intatta inviando un pacchetto Keep Alive. Un sistema remoto raggiungibile riconoscerà la trasmissione Keep-Alive. I pacchetti Keep Alive non vengono inviati per impostazione predefinita. Questa funzionalità può essere abilitata in una connessione da un'applicazione. Valore predefinito: 7.200.000 (due ore).

</dd> <dt>

**Macaddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni di input e output del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Indirizzo MAC (Media Access Control) della scheda di rete. Un indirizzo MAC viene assegnato dal produttore per identificare in modo univoco la scheda di rete.

Esempio: "00:80:C7:8F:6C:96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Esegue l'override dell'unità massima di trasmissione (MTU) predefinita per un'interfaccia di rete. Il valore MTU è la dimensione massima del pacchetto (inclusa l'intestazione del trasporto) che il trasporto trasmetterà sulla rete sottostante. Il datagramma IP può estendersi su più pacchetti. L'intervallo di questo valore si estende tra le dimensioni minime del pacchetto (68) e le MTU supportate dalla rete sottostante.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| NumForwardPackets")
</dt> </dl>

Numero di intestazioni di pacchetti IP allocate per la coda di pacchetti del router. Quando tutte le intestazioni sono in uso, il router inizierà a rimuovere i pacchetti dalla coda in modo casuale. Questo valore deve essere almeno pari al valore **ForwardBufferMemory** diviso per le dimensioni massime dei dati IP delle reti connesse al router. Non deve essere maggiore del valore **ForwardBufferMemory** diviso per 256, poiché per ogni pacchetto vengono usati almeno 256 byte di memoria del buffer di inoltro. Il numero ottimale di pacchetti di inoltro per una determinata **dimensione ForwardBufferMemory** dipende dal tipo di traffico sulla rete. Sarà compreso tra questi due valori. Se il router non è abilitato, questo parametro viene ignorato e non viene allocata alcuna intestazione. Impostazione predefinita: 50, Intervallo valido: 1 - 0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUBHDetect")
</dt> </dl>

Se **TRUE,** il rilevamento dei router black hole si verifica mentre TCP individua il percorso dell'unità di trasmissione massima. Un router black hole non restituisce messaggi ICMP destination Unreachable quando deve frammentare un datagramma IP con il bit Don't Fragment impostato. TCP dipende dalla ricezione di questi messaggi per eseguire l'individuazione MTU del percorso. Con questa funzionalità abilitata, TCP tenterà di inviare segmenti senza il bit Don't Fragment impostato se diverse ritrasmissioni di un segmento non vengono riconoscite. Se il segmento viene riconosciuto come risultato, mss verrà ridotto e il bit Don't Fragment verrà impostato nei pacchetti futuri nella connessione. L'abilitazione del rilevamento dei black hole aumenta il numero massimo di ritrasmissioni eseguite per un determinato segmento. Il valore predefinito di questa proprietà è **FALSE.**

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| EnablePMTUDiscovery")
</dt> </dl>

Se **TRUE,** il percorso MTU (Maximum Transmission Unit) viene individuato nel percorso di un host remoto. Individuando il percorso MTU e limitando i segmenti TCP a queste dimensioni, TCP può eliminare la frammentazione nei router lungo il percorso che connettono reti con MTU diverse. La frammentazione influisce negativamente sulla velocità effettiva TCP e sulla congestione della rete. L'impostazione di questo parametro su **FALSE** comporta l'uso di un MTU di 576 byte per tutte le connessioni che non sono a computer nella subnet locale. Il valore predefinito è **TRUE.**

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nome del servizio della scheda di rete. Questo nome è in genere più breve del nome completo del prodotto.

Esempio: "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Mappa di bit delle possibili impostazioni correlate a NetBIOS su TCP/IP. I valori sono identificati nell'elenco seguente.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxConnectRetransmissions")
</dt> </dl>

Numero di tentativi TCP di ritrasmissione di una richiesta di connessione prima di terminare la connessione. Il timeout di ritrasmissione iniziale è di 3 secondi. Il timeout di ritrasmissione raddoppia per ogni tentativo. Impostazione predefinita: 3, Intervallo valido: 0 - 0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpMaxDataRetransmissions")
</dt> </dl>

Numero di volte in cui TCP ritrasmette un singolo segmento di dati (segmento non di connessione) prima di terminare la connessione. Il timeout di ritrasmissione raddoppia a ogni successiva ritrasmissione in una connessione. Valore predefinito: 5, Intervallo valido: 0 - 0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpNumConnections")
</dt> </dl>

Numero massimo di connessioni che TCP può aprire contemporaneamente. Impostazione predefinita: 0xFFFFFE, Intervallo valido: 0 - 0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Se **TRUE,** TCP usa la specifica RFC 1122 per i dati urgenti. Se **FALSE** (impostazione predefinita), TCP usa la modalità usata dai sistemi derivati da Berkeley Software Design (BSD). I due meccanismi interpretano il puntatore urgente in modo diverso e non sono interoperativi. Il valore predefinito è **FALSE.**

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Dimensioni massime della finestra di ricezione TCP offerte dal sistema. La finestra di ricezione specifica il numero di byte che un mittente può trasmettere senza ricevere un riconoscimento. In generale, le finestre ricevente più grandi miglioreranno le prestazioni rispetto alle reti a ritardo elevato e a larghezza di banda elevata. Per migliorare l'efficienza, la finestra ricevente deve essere un multiplo pari delle dimensioni massime del segmento TCP (MSS). Impostazione predefinita: quattro volte le dimensioni massime dei dati TCP o un multiplo pari delle dimensioni dei dati TCP arrotondato al multiplo più vicino di 8192. Per impostazione predefinita, le reti Ethernet sono 8760. Intervallo valido: da 0 a 65535.

> [!Note]  
> Windows Vista: questa proprietà accede alla voce del Registro di sistema, che `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` non viene usata nell'implementazione corrente del sistema operativo.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services Parametri \\ \\ Tcpip \\ \\ \| EnableLMHOSTS")
</dt> </dl>

Se **TRUE,** vengono usati i file di ricerca locali. I file di ricerca conterranno una mappa di indirizzi IP ai nomi host. Se esistono nel sistema locale, si trovano in %SystemRoot% \\ system32 \\ driver e così \\ via.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)drivers etc \| \\ \\ \\ \\ \\ \\ lmhosts")
</dt> </dl>

Percorso di un file di ricerca WINS nel sistema locale. Questo file conterrà una mappa di indirizzi IP ai nomi host. Se il file specificato in questa proprietà viene trovato, verrà copiato nella cartella %SystemRoot% \\ driver system32 e così via del sistema \\ \\ locale. Valido solo se la **proprietà WINSEnableLMHostsLookup** è **TRUE.**

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni di input e output del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Indirizzo IP per il server WINS primario.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip Parameters \\ \\ \| ScopeID")
</dt> </dl>

Valore aggiunto alla fine del nome NetBIOS che isola un gruppo di sistemi di computer che comunicano solo tra loro. Viene usato per tutte le transazioni NetBIOS su comunicazioni TCP/IP dal sistema informatico. I computer configurati con identificatori di ambito identici sono in grado di comunicare con questo computer. I client TCP/IP con identificatori di ambito diversi ignorano i pacchetti provenienti dai computer con questo identificatore di ambito. Valido solo quando il [**metodo EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) viene eseguito correttamente.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni di input e output del dispositivo Win32API \| \| DeviceIoControl")
</dt> </dl>

Indirizzo IP per il server WINS secondario.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ NetworkAdapterConfiguration Win32** deriva dall'impostazione [**CIM \_**](cim-setting.md).

## <a name="examples"></a>Esempio

L'esempio di codice VBScript di [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) in TechNet Gallery usa la **classe \_ NetworkAdapterConfiguration Win32** per recuperare le informazioni di configurazione di rete da diversi computer remoti.

L'esempio [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI) PowerShell (Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in TechNet Gallery usa una serie di chiamate all'hardware e al software, tra cui **\_ NetworkAdapterConfiguration Win32,** per visualizzare informazioni su un sistema locale o remoto.

Il codice di PowerShell seguente recupera le impostazioni di configurazione per l'adapter Microsoft ISTAP.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



Nell'esempio C \# seguente vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete. Si noti che in questo esempio C viene utilizzato lo spazio dei nomi \# [Microsoft.Management.Infrastructure,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) che in genere viene ridimensionato in modo più efficiente rispetto alle classi WMI dello spazio dei [nomi System.Management.](/dotnet/api/system.management)


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



Nell'esempio C \# seguente vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete. Si noti che in questo esempio C viene utilizzato lo spazio dei nomi \# [System.Management](/dotnet/api/system.management) originale, sostituito da [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



Nell'esempio seguente vengono recuperate informazioni **dalla classe \_ NetworkAdapterConfiguration Win32.**


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> <dt>

[Attività WMI: Rete](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Attività WMI: Account e domini](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Supporto di IPv6 e IPv4 in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 

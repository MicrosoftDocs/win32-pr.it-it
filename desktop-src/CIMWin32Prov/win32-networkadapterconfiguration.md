---
description: Rappresenta gli attributi e i comportamenti di una scheda di rete. Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendente dalla scheda di rete.
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
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127470"
---
# <a name="win32_networkadapterconfiguration-class"></a>Win32 \_ NetworkAdapterConfiguration (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterConfiguration Win32** rappresenta gli attributi e i comportamenti di una scheda di rete. Questa classe include proprietà e metodi aggiuntivi che supportano la gestione del protocollo TCP/IP indipendente dalla scheda di rete.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ NetworkAdapterConfiguration** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ NetworkAdapterConfiguration** presenta questi metodi.



| Metodo                                                                                                                       | Descrizione                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Disabilita IPsec in questa scheda di rete abilitata per TCP/IP.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Abilita il Dynamic Host Configuration Protocol (DHCP) per il servizio con questa scheda di rete.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Abilita il Domain Name System (DNS) per il servizio in questa scheda di rete associata a TCP/IP.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Abilita IPsec a livello globale in tutte le schede di rete con binding IP.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Abilita IPsec su questa specifica scheda di rete abilitata per TCP/IP.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Abilita l'indirizzamento TCP/IP statico per la scheda di rete di destinazione.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Abilita le impostazioni WINS specifiche per TCP/IP, ma indipendente dalla scheda di rete.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Rilascia l'indirizzo IP associato a una specifica scheda di rete abilitata per DHCP.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Rilascia gli indirizzi IP associati a tutte le schede di rete abilitate per DHCP.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Rinnovare l'indirizzo IP in specifiche schede di rete abilitate per DHCP.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Rinnova gli indirizzi IP in tutte le schede di rete abilitate per DHCP.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta la trasmissione di query ARP da parte del protocollo TCP/IP.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Consente ai pacchetti Ethernet di usare la codifica SNAP 802,3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Imposta il percorso dei file di database Internet standard (host, LMHOSTS, reti e protocolli).<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Abilita il rilevamento del gateway non attivo.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Obsoleta. Questo metodo imposta il valore predefinito del tipo di servizio (TOS) nell'intestazione dei pacchetti IP in uscita.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Imposta il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Imposta il dominio DNS.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta l'ordine di ricerca del server sotto forma di matrice di elementi.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Imposta l'ordine di ricerca dei suffissi come una matrice di elementi.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Indica la registrazione DNS dinamica degli indirizzi IP per questa scheda associata a IP.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Specifica la quantità di memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router.<br/>                                                    |
| [**Gateway**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Specifica un elenco di gateway per il routing dei pacchetti destinati a una subnet diversa da quella a cui è connessa questa scheda.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Imposta la misura in cui il sistema supporta il multicast IP e partecipa al protocollo di gestione dei gruppi Internet.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Imposta la metrica di routing associata a questo adapter associato a IP.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Imposta l'utilizzo broadcast IP zero.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Imposta le coppie di fotogrammi/numero di rete IPX (Internetworking Packet Exchange) per questa scheda di rete.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta l'intervallo che separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Imposta la frequenza con cui TCP tenta di verificare che una connessione inattiva sia ancora disponibile inviando un pacchetto keep-alive.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Imposta l'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.<br/> Questo metodo non è supportato.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta il numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Abilita il rilevamento di router black hole.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Abilita l'individuazione dell'unità di trasmissione massima (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios consente**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Imposta l'operazione predefinita di NetBIOS su TCP/IP.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Imposta il numero di tentativi TCP per la ritrasmissione di una richiesta di connessione prima dell'interruzione.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Imposta il numero di volte in cui TCP ritrasmetterà un singolo segmento di dati prima di interrompere la connessione.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Imposta il numero massimo di connessioni che TCP potrebbe avere aperto simultaneamente.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Specifica se TCP utilizza la specifica RFC 1122 per i dati urgenti o la modalità utilizzata dai sistemi derivati da Berkeley Software Design (BSD).<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Imposta le dimensioni massime della finestra di ricezione TCP offerte dal sistema.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Imposta i server WINS (Windows Internet Naming Service) primari e secondari in questa scheda di rete associata a TCP/IP.<br/>                        |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ NetworkAdapterConfiguration** dispone di queste proprietà.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

Se **true**, TCP/IP trasmette le query ARP (Address Resolution Protocol) con il routing del codice sorgente abilitato nelle reti token ring. Per impostazione predefinita (FALSE), ARP esegue prima una query senza routing del codice sorgente, quindi tenta di eseguire il routing del codice sorgente se non viene ricevuta alcuna risposta. Il routing del codice sorgente consente il routing dei pacchetti di rete tra diversi tipi di reti.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

Se il valore è **true**, i pacchetti Ethernet seguono la codifica di SNAP (Sub-Network Access Protocol) IEEE 802,3. Impostando questo parametro su 1 si impone a TCP/IP di trasmettere i pacchetti Ethernet utilizzando la codifica di SNAP 802,3. Per impostazione predefinita (FALSE), lo stack trasmette i pacchetti in formato Ethernet DIX.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Percorso file di Windows valido per i file di database Internet standard (host, LMHOSTS, reti e protocolli). Il percorso del file viene utilizzato dall'interfaccia Windows Sockets.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

Se **true**, si verifica il rilevamento del gateway inattivo. Se questa funzionalità è abilitata, Transmission Control Protocol (TCP) richiede il protocollo IP (Internet Protocol) per passare a un gateway di backup se ritrasmette un segmento più volte senza ricevere una risposta.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| GatewayPredefinito")
</dt> </dl>

Matrice di indirizzi IP di gateway predefiniti usati dal computer.

Esempio: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Valore predefinito del tipo di servizio (TOS) impostato nell'intestazione dei pacchetti IP in uscita. La richiesta di commenti (RFC) 791 definisce i valori. Valore predefinito: 0 (zero), intervallo valido: 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| DefaultTTL")
</dt> </dl>

Valore predefinito TTL (time to Live) impostato nell'intestazione dei pacchetti IP in uscita. La durata (TTL) specifica il numero di router che un pacchetto IP può attraversare per raggiungere la destinazione prima di essere scartato. Ogni router decrementa di uno il numero di TTL di un pacchetto mentre passa attraverso ed Elimina i pacchetti, se il valore TTL è 0 (zero). Valore predefinito: 32, intervallo valido: 1-255.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

Se **true**, il server DHCP (Dynamic Host Configuration Protocol) assegna automaticamente un indirizzo IP al sistema quando stabilisce una connessione di rete.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Data e ora di scadenza per un indirizzo IP con lease assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).

Esempio: 20521201000230,000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Data e ora in cui è stato ottenuto il lease per l'indirizzo IP assegnato al computer dal server DHCP (Dynamic Host Configuration Protocol).

Esempio: 19521201000230,000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| dhcpserver")
</dt> </dl>

Indirizzo IP del server DHCP (Dynamic Host Configuration Protocol).

Esempio: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| Domain")
</dt> </dl>

Nome dell'organizzazione seguito da un punto e un'estensione che indica il tipo di organizzazione, ad esempio "microsoft.com". Il nome può essere una qualsiasi combinazione di lettere da A A Z, i numeri da 0 A 9 e il trattino (-), più il carattere punto (.) utilizzato come separatore.

Esempio: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| Searching")
</dt> </dl>

Matrice di suffissi di dominio DNS da accodare alla fine dei nomi host durante la risoluzione del nome. Quando si tenta di risolvere un nome di dominio completo (FQDN) da un nome di solo host, il sistema aggiungerà prima di tutto il nome di dominio locale. Se l'operazione non riesce, il sistema utilizzerà l'elenco dei suffissi di dominio per creare nomi di dominio completi aggiuntivi nell'ordine elencato ed eseguirà una query sui server DNS per ciascuno di essi.

Esempio: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableDNS")
</dt> </dl>

Se **true**, il Domain Name System (DNS) è abilitato per la risoluzione dei nomi sulla risoluzione di Windows Internet Naming Service (WINS). Se il nome non può essere risolto con DNS, la richiesta del nome viene trasmessa a WINS per la risoluzione.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| hostname")
</dt> </dl>

Nome host utilizzato per identificare il computer locale per l'autenticazione da parte di alcune utilità. Altre utilità basate su TCP/IP possono usare questo valore per acquisire il nome del computer locale. I nomi host vengono archiviati nei server DNS di una tabella che esegue il mapping dei nomi agli indirizzi IP per l'utilizzo da DNS. Il nome può essere una qualsiasi combinazione di lettere da A A Z, i numeri da 0 A 9 e il trattino (-), più il carattere punto (.) utilizzato come separatore. Per impostazione predefinita, questo valore è il nome del computer di rete Microsoft, ma l'amministratore di rete può assegnare un altro nome host senza influire sul nome del computer.

Esempio: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| nameserver")
</dt> </dl>

Matrice di indirizzi IP del server da utilizzare nell'esecuzione di query per i server DNS.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, gli indirizzi IP per questa connessione vengono registrati in DNS con il nome di dominio della connessione, oltre a essere registrati con il nome DNS completo del computer. Il nome di dominio della connessione viene impostato tramite il metodo [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() o assegnato da DSCP. Il nome registrato è il nome host del computer a cui è stato aggiunto il nome di dominio.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router. Quando lo spazio del buffer viene riempito, il router inizia a scartare i pacchetti in modo casuale dalla propria coda. I buffer di dati della coda di pacchetti hanno una lunghezza di 256 byte, quindi il valore di questo parametro deve essere un multiplo di 256. Più buffer vengono concatenati per i pacchetti più grandi. L'intestazione IP per un pacchetto viene archiviata separatamente. Questo parametro viene ignorato e non vengono allocati buffer se il router IP non è abilitato. La dimensione del buffer può variare dall'MTU di rete a un valore inferiore a 0xFFFFFFFF. Valore predefinito: 74240 (pacchetti da 50 1480 byte, arrotondati a un multiplo di 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, gli indirizzi IP per questa connessione sono registrati in DNS con il nome DNS completo del computer. Il nome DNS completo del computer viene visualizzato nella scheda **Identificazione rete** dell'applicazione di sistema nel pannello di controllo.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di valori di metrica dei costi interi (compresi tra 1 e 9999) da usare per il calcolo delle route più veloci, più affidabili o meno a elevato utilizzo di risorse. Questo argomento ha una corrispondenza uno-a-uno con la proprietà **DefaultIPGateway** .

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Extent a cui il sistema supporta il multicast IP e partecipa al protocollo IGMP (Internet Group Management Protocol). Al livello 0 (zero), il sistema non fornisce alcun supporto per il multicast. Al livello 1, il sistema può inviare solo pacchetti multicast IP. Al livello 2, il sistema può inviare pacchetti multicast IP e partecipare completamente a IGMP per ricevere pacchetti multicast.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Nessun multicast** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**Multicast IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**Multicast IP & IGMP** (2)


</dt> <dd>

Multicast IP e IGMP (impostazione predefinita)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Numero di indice della configurazione della scheda di rete Windows. Il numero di indice viene usato quando è disponibile più di una configurazione.

</dd> <dt>

**IndiceInterfaccia**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di indice che identifica in modo univoco un'interfaccia di rete locale. Il valore in questa proprietà corrisponde al valore della proprietà **IndiceInterfaccia** nell'istanza di [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) che rappresenta l'interfaccia di rete nella tabella di route.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ TCPIP \| IPAddress")
</dt> </dl>

Matrice di tutti gli indirizzi IP associati alla scheda di rete corrente. Questa proprietà può contenere indirizzi IPv6 o IPv4. Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Esempio di indirizzo IPv6: "2010:836B: 4179:: 836B: 4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Costo dell'utilizzo delle route configurate per l'adapter associato IP ed è il valore ponderato per le route nella tabella di routing IP. Se sono presenti più route a una destinazione nella tabella di routing IP, viene utilizzata la route con la metrica più bassa. Il valore predefinito è 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")
</dt> </dl>

Se **true**, TCP/IP è associato e abilitato in questa scheda di rete.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| IPFilterSecurityEnabled")
</dt> </dl>

Se **true**, la sicurezza della porta IP è abilitata a livello globale in tutte le schede di rete associate a IP e i valori di sicurezza associati alle singole schede di rete sono attivati. Questa proprietà viene utilizzata insieme a **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** e **IPSecPermitIPProtocols**. Se **false**, la sicurezza del filtro IP viene disabilitata in tutte le schede di rete e consente il flusso non filtrato di tutto il traffico di porta e protocollo.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

Se **true**, la sicurezza della porta IP è abilitata a livello globale in tutte le schede di rete con binding IP. Questa proprietà è obsoleta. Al posto di questa proprietà, è consigliabile usare **IPFilterSecurityEnabled**.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| RawIPAllowedProtocols")
</dt> </dl>

Matrice dei protocolli di cui è consentita l'esecuzione su IP. L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . L'elenco può essere vuoto o contenere valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutti i protocolli. Una stringa vuota indica che non è consentita l'esecuzione di protocolli quando **IPFilterSecurityEnabled** è **true**.

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TCPAllowedPorts")
</dt> </dl>

Matrice delle porte a cui verrà concessa l'autorizzazione di accesso per TCP. L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . L'elenco può essere vuoto o contenere valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte. Una stringa vuota indica che alle porte non è concessa l'autorizzazione di accesso quando **IPFilterSecurityEnabled** è **true**.

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| UDPAllowedPorts")
</dt> </dl>

Matrice delle porte a cui verrà concessa l'autorizzazione di accesso UDP (User Datagram Protocol). L'elenco di protocolli viene definito utilizzando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) . L'elenco può essere vuoto o contenere valori numerici. Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte. Una stringa vuota indica che alle porte non è concessa l'autorizzazione di accesso quando **IPFilterSecurityEnabled** è **true**.

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| \| submask Parameters")
</dt> </dl>

Matrice di tutte le subnet mask associate alla scheda di rete corrente.

Esempio: "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| parametro UseZeroBroadcast")
</dt> </dl>

Se **true**, vengono usati gli zeri IP-broadcast (0.0.0.0) e il sistema usa le trasmissioni-broadcast (255.255.255.255). I sistemi informatici usano in genere le trasmissioni, ma quelle derivate dalle implementazioni di BSD usano gli zeri. I sistemi che non utilizzano le stesse trasmissioni non interagiscono nella stessa rete. Il valore predefinito è **false**.

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets versione 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| PktType")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Snap** -in Ethernet (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Automatico** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| mediaType")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

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

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| numerorete")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ NWLNKIPX \\ \\ Parameters \| VirtualNetworkNumber")
</dt> </dl>

La tecnologia IPX (Internet-Packet Exchange) non è più supportata e questa proprietà non contiene dati utili.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| keepAliveInterval"), [**unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")
</dt> </dl>

L'intervallo separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta. Dopo la ricezione di una risposta, il ritardo fino a quando la trasmissione Keep-Alive successiva viene nuovamente controllata dal valore di **KeepAliveTime**. La connessione verrà interrotta dopo che il numero di ritrasmissioni specificato da **TcpMaxDataRetransmissions** non è stato risposto. Valore predefinito: 1000, intervallo valido: 1-0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| keepAliveInterval"), [**unità**](../wmisdk/standard-qualifiers.md) ("millisecondi")
</dt> </dl>

La proprietà **KeepAliveTime** indica la frequenza con cui il protocollo TCP tenta di verificare che una connessione inattiva sia ancora intatta inviando un pacchetto keep-alive. Un sistema remoto raggiungibile rileverà la trasmissione keep-alive. I pacchetti Keep-Alive non vengono inviati per impostazione predefinita. Questa funzionalità può essere abilitata in una connessione da un'applicazione. Valore predefinito: 7,2 milioni (due ore).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")
</dt> </dl>

Indirizzo MAC (Media Access Control) della scheda di rete. Un indirizzo MAC viene assegnato dal produttore per identificare in modo univoco la scheda di rete.

Esempio: "00:80: C7:8F: 6C: 96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Esegue l'override dell'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete. MTU è la dimensione massima del pacchetto (inclusa l'intestazione di trasporto) che il trasporto trasmetterà sulla rete sottostante. Il datagramma IP può estendersi su più pacchetti. L'intervallo di questo valore si estende alla dimensione minima del pacchetto (68) al valore MTU supportato dalla rete sottostante.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| NumForwardPackets")
</dt> </dl>

Numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router. Quando tutte le intestazioni sono in uso, il router inizierà a eliminare i pacchetti dalla coda in modo casuale. Questo valore deve essere almeno uguale al valore di **ForwardBufferMemory** diviso per la dimensione massima dei dati IP delle reti connesse al router. Il valore non deve essere maggiore del valore di **ForwardBufferMemory** diviso per 256, poiché per ogni pacchetto vengono utilizzati almeno 256 byte di memoria del buffer di avanzamento. Il numero ottimale di pacchetti di avanzamento per una determinata dimensione di **ForwardBufferMemory** dipende dal tipo di traffico sulla rete. Tra questi due valori. Se il router non è abilitato, questo parametro viene ignorato e non vengono allocate intestazioni. Valore predefinito: 50, intervallo valido: 1-0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

Se **true**, il rilevamento di router black hole si verifica mentre TCP individua il percorso dell'unità di trasmissione massima. Un router black hole non restituisce messaggi non raggiungibili della destinazione ICMP quando è necessario frammentare un datagramma IP con il bit not Fragment impostato. TCP dipende dalla ricezione di questi messaggi per l'esecuzione dell'individuazione MTU del percorso. Se questa funzionalità è abilitata, TCP tenterà di inviare segmenti senza il bit non frammento impostato se diverse ritrasmissioni di un segmento non vengono riconosciute. Se il segmento viene riconosciuto come risultato, la MSS verrà ridotta e il bit not Fragment verrà impostato in pacchetti futuri sulla connessione. L'abilitazione del rilevamento di buchi neri aumenta il numero massimo di ritrasmissioni eseguite per un determinato segmento. Il valore predefinito di questa proprietà è **false**.

</dd> <dt>

**PMTUDiscoveryEnabled consente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

Se **true**, il percorso dell'unità di trasmissione massima (MTU) viene individuato sul percorso di un host remoto. Scoprendo il percorso MTU e limitando i segmenti TCP a queste dimensioni, TCP può eliminare la frammentazione nei router lungo il percorso che connette le reti con MTU diversi. La frammentazione influisce negativamente sulla velocità effettiva TCP e sulla congestione della rete. Impostando questo parametro su **false** , viene usato un MTU di 576 byte per tutte le connessioni che non sono computer nella subnet locale. Il valore predefinito è **true**.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nome del servizio della scheda di rete. Questo nome è in genere più breve del nome completo del prodotto.

Esempio: "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bitmap delle possibili impostazioni correlate a NetBIOS su TCP/IP. I valori sono identificati nell'elenco seguente.

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

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxConnectRetransmissions")
</dt> </dl>

Numero di tentativi effettuati da TCP per ritrasmettere una richiesta di connessione prima di terminare la connessione. Il timeout di ritrasmissione iniziale è di 3 secondi. Il timeout di ritrasmissione raddoppia per ogni tentativo. Valore predefinito: 3, intervallo valido: 0-0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpMaxDataRetransmissions")
</dt> </dl>

Numero di volte in cui TCP ritrasmette un singolo segmento di dati (segmento non di connessione) prima di terminare la connessione. Il timeout di ritrasmissione raddoppia con ogni ritrasmissione successiva in una connessione. Valore predefinito: 5, intervallo valido: 0-0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpNumConnections")
</dt> </dl>

Numero massimo di connessioni che TCP può aprire contemporaneamente. Impostazione predefinita: 0xFFFFFE, intervallo valido: 0-0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

Se **true**, TCP utilizza la specifica RFC 1122 per i dati urgenti. Se **false** (impostazione predefinita), TCP utilizza la modalità utilizzata dai sistemi derivati di Berkeley Software Design (BSD). I due meccanismi interpretano il puntatore urgente in modo diverso e non sono interoperativi. Il valore predefinito è **false**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Dimensioni massime della finestra di ricezione TCP offerte dal sistema. Nella finestra di ricezione viene specificato il numero di byte che un mittente può trasmettere senza ricevere un riconoscimento. In generale, le finestre di ricezione più grandi migliorano le prestazioni rispetto alle reti ad alto ritardo e a larghezza di banda elevata. Per migliorare l'efficienza, la finestra di ricezione deve essere un multiplo pari delle dimensioni del segmento massimo TCP (MSS). Impostazione predefinita: quattro volte la dimensione massima dei dati TCP o un multiplo pari delle dimensioni dei dati TCP arrotondati al multiplo più vicino di 8192. Il valore predefinito per le reti Ethernet è 8760. Intervallo valido: 0-65535.

> [!Note]  
> Windows Vista: questa proprietà accede alla `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` voce del registro di sistema, che non viene usata nell'implementazione corrente del sistema operativo.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| EnableLMHOSTS")
</dt> </dl>

Se **true**, vengono usati i file di ricerca locali. I file di ricerca conterranno una mappa degli indirizzi IP ai nomi host. Se sono presenti nel sistema locale, saranno disponibili in% SystemRoot% \\ system32 \\ drivers e \\ così via.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ LMHOSTS")
</dt> </dl>

Percorso di un file di ricerca WINS nel sistema locale. Questo file conterrà una mappa degli indirizzi IP ai nomi host. Se il file specificato in questa proprietà viene trovato, verrà copiato nella cartella% SystemRoot% \\ system32 \\ drivers \\ del sistema locale. Valido solo se la proprietà **WINSEnableLMHostsLookup** è **true**.

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")
</dt> </dl>

Indirizzo IP del server WINS primario.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ TCPIP \\ \\ Parameters \| elemento ScopeId")
</dt> </dl>

Valore aggiunto alla fine del nome NetBIOS che isola un gruppo di sistemi informatici che comunicano tra loro. Viene utilizzato per tutte le transazioni NetBIOS su comunicazioni TCP/IP dal sistema del computer. I computer configurati con identificatori di ambito identici sono in grado di comunicare con questo computer. I client TCP/IP con identificatori di ambito diversi ignorano i pacchetti provenienti da computer con questo identificatore di ambito. Valido solo quando il metodo [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) viene eseguito correttamente.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| device input and Output functions \| DeviceIoControl")
</dt> </dl>

Indirizzo IP del server WINS secondario.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ NetworkAdapterConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript [Information Retriever WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) della raccolta TechNet viene utilizzata la classe **Win32 \_ NetworkAdapterConfiguration** per recuperare le informazioni di configurazione di rete da un numero di computer remoti.

L'esempio relativo a [Get-ComputerInfo-query computer da computer locale/remoto-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell nella raccolta TechNet usa una serie di chiamate a hardware e software, tra cui **Win32 \_ NetworkAdapterConfiguration**, per visualizzare informazioni su un sistema locale o remoto.

Il codice di PowerShell seguente consente di recuperare le impostazioni di configurazione per l'adapter Microsoft ISTAP.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



Nell'esempio C seguente \# vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete. Si noti che \# in questo esempio C viene utilizzato lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , che in genere è più efficiente delle classi WMI dello spazio dei nomi [System. Management](/dotnet/api/system.management) .


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



Nell'esempio C seguente \# vengono recuperati la descrizione e il numero di indice di tutte le istanze di configurazione della scheda di rete. Si noti che \# in questo esempio C viene utilizzato lo spazio dei nomi [System. Management](/dotnet/api/system.management) originale, che è stato sostituito da [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).


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



Nell'esempio seguente vengono recuperate le informazioni dalla classe **Win32 \_ NetworkAdapterConfiguration** .


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



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> <dt>

[Attività WMI: rete](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Attività WMI: account e domini](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[Supporto di IPv6 e IPv4 in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 

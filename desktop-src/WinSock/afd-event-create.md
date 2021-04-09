---
description: Evento di traccia di rete Winsock per un'operazione di creazione del socket.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: Evento AFD_EVENT_CREATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879241"
---
# <a name="afd_event_create-event"></a>\_Evento di \_ creazione evento AFD

L'evento di **\_ \_ creazione evento AFD** è un evento di traccia di rete Winsock per un'operazione di creazione del socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informazioni su questo evento.

Nella tabella seguente sono elencati i valori possibili per il parametro *EnterExit* :



| Valore                                                                        | Significato                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inizio di una richiesta Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | La richiesta Winsock è stata completata.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Il driver AFD Winsock ha intrapreso un'azione interna (ad esempio, l'interruzione di una connessione).<br/>      |
| <dl> <dt>3</dt> </dl> | Questo evento è stato generato dal driver TCP/IP. Questo indica in genere una notifica dei dati.<br/> |
| <dl> <dt>4</dt> </dl> | Il driver AFD Winsock ha causato il verificarsi di questo evento (ad esempio, l'impostazione di un'opzione socket).<br/> |



 

</dd> <dt>

*Posizione* 
</dt> <dd>

Campo privato utilizzato internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

Indirizzo [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del processo a cui appartiene il socket correlato. Si tratta di una struttura opaca che funge da oggetto processo per un processo. Per ulteriori informazioni, vedere la documentazione del kit driver Windows per la struttura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Endpoint* 
</dt> <dd>

Indirizzo dell' \_ endpoint AFD del socket.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

Specifica della famiglia di indirizzi per il socket. I valori possibili per la famiglia di indirizzi sono definiti nel file di intestazione *Ws2def. h* . Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

I valori attualmente supportati sono AF \_ inet o AF \_ INET6, ovvero i formati della famiglia di indirizzi Internet per IPv4 e IPv6. Sono supportate altre opzioni per la famiglia di indirizzi (ad \_ esempio, AF NetBIOS per l'uso con NetBIOS) se è installato un provider di servizi Windows Sockets per la famiglia di indirizzi.

La tabella seguente elenca i valori comuni per la famiglia di indirizzi, sebbene siano possibili molti altri valori.



| AF                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ Unspect**</dt> <dt>0</dt> </dl>           | La famiglia di indirizzi non è specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Famiglia di indirizzi protocollo Internet versione 4 (IPv4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Famiglia di indirizzi IPX/SPX. Questa famiglia di indirizzi è supportata solo se è installato il protocollo di trasporto compatibile con NWLink IPX/SPX NetBIOS. <br/> Questa famiglia di indirizzi non è supportata in Windows Vista e versioni successive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Famiglia di indirizzi AppleTalk. Questa famiglia di indirizzi è supportata solo se il protocollo AppleTalk è installato. <br/> Questa famiglia di indirizzi non è supportata in Windows Vista e versioni successive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | Famiglia di indirizzi NetBIOS. Questa famiglia di indirizzi è supportata solo se è installato il provider Windows Sockets per NetBIOS. <br/> Il provider Windows Sockets per NetBIOS è supportato nelle versioni di Windows a 32 bit. Questo provider viene installato per impostazione predefinita nelle versioni di Windows a 32 bit. <br/> Il provider Windows Sockets per NetBIOS non è supportato nelle versioni di Windows a 64 bit. <br/> Il provider Windows Sockets per NetBIOS supporta solo socket in cui il parametro di *tipo* è impostato su **Sock \_ DGRAM**.<br/> Il provider Windows Sockets per NetBIOS non è direttamente correlato all'interfaccia di programmazione [NetBIOS](/previous-versions/windows/desktop/netbios/portal) . L'interfaccia di programmazione NetBIOS non è supportata in Windows Vista, Windows Server 2008 e versioni successive.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | Famiglia di indirizzi protocollo Internet versione 6 (IPv6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | Famiglia di indirizzi IrDA (Infrared Data Association). <br/> Questa famiglia di indirizzi è supportata solo se il computer dispone di una porta e di un driver infrarossi installati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Famiglia di indirizzi Bluetooth. <br/> Questa famiglia di indirizzi è supportata solo se nel computer è installato un adattatore e un driver Bluetooth.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

Specifica del tipo per il nuovo socket. I valori possibili per il tipo di socket sono definiti nel file di intestazione *Winsock2. h* .

Nella tabella seguente sono elencati i valori possibili per il parametro di *tipo* supportato per Windows Sockets 2:



| Type                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**Calzino \_ FLUSSO**</dt> <dt>1</dt> </dl>          | Tipo di socket che fornisce flussi di byte sequenziati, affidabili, bidirezionali e basati sulla connessione con un meccanismo di trasmissione dati OOB. Questo tipo di socket usa il Transmission Control Protocol (TCP) per la famiglia di indirizzi Internet (AF \_ inet o AF \_ INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**Calzino \_ DGRAM**</dt> <dt>2</dt> </dl>             | Tipo di socket che supporta datagrammi, che sono buffer senza connessione e non affidabili di una lunghezza massima fissa (in genere piccola). Questo tipo di socket usa il protocollo UDP (User Datagram Protocol) per la famiglia di indirizzi Internet (AF \_ inet o AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**Calzino \_ RAW**</dt> <dt>3</dt> </dl>                   | Tipo di socket che fornisce un socket non elaborato che consente a un'applicazione di modificare l'intestazione del protocollo di livello superiore successivo. Per modificare l'intestazione IPv4, è necessario impostare l'opzione del socket [**\_ HDRINCL IP**](ipproto-ip-socket-options.md) sul socket. Per modificare l'intestazione IPv6, è necessario impostare l'opzione socket [**IPv6 \_ HDRINCL**](ipproto-ipv6-socket-options.md) sul socket. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**Calzino \_ RDM**</dt> <dt>4</dt> </dl>                   | Tipo di socket che fornisce un datagramma di messaggio affidabile. Un esempio di questo tipo è l'implementazione del protocollo multicast PGM (Pragmatic General Multicast) in Windows, spesso definita [programmazione multicast affidabile](reliable-multicast-programming--pgm-.md). <br/> Il valore di questo *tipo* è supportato solo se è installato il protocollo multicast affidabile.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**Calzino \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Tipo di socket che fornisce un pacchetto pseudo-flusso basato su datagrammi. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocollo* 
</dt> <dd>

Protocollo da utilizzare. Le opzioni possibili per il parametro del *protocollo* sono specifiche per la famiglia di indirizzi e il tipo di socket specificati. I valori possibili per il *protocollo* vengono definiti nel file *di intestazione di* gestione risorse di gestione e nel tipo di enumerazione **IPPROTO** definito nel file di intestazione *Ws2def. h* . Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

Se viene specificato un valore pari a 0, il chiamante non desidera specificare un protocollo e il provider di servizi sceglierà il *protocollo* da utilizzare.

La tabella seguente elenca i valori comuni per il *protocollo* , sebbene siano possibili molti altri valori.



| protocol                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Il Internet Control Message Protocol (ICMP). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ UNSPEC**, **AF \_ inet** o **AF \_ INET6** e il  parametro di tipo **è \_ RAW** o Unspecified.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | Il protocollo IGMP (Internet Group Management Protocol). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ UNSPEC**, **AF \_ inet** o **AF \_ INET6** e il  parametro di tipo **è \_ RAW** o Unspecified.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | Protocollo Bluetooth RFCOMM (Radio Frequency Communications). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ BTH** e il parametro di *tipo* è **Sock \_ Stream**. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | Il Transmission Control Protocol (TCP). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ inet** o **AF \_ INET6** e il parametro di *tipo* è **Sock \_ Stream**.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Il protocollo UDP (User Datagram Protocol). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ inet** o **AF \_ INET6** e il parametro di *tipo* è **Sock \_ DGRAM**.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | Il Internet Control Message Protocol versione 6 (ICMPv6). Si tratta di un valore possibile quando il parametro *AF* è **AF \_ UNSPEC**, **AF \_ inet** o **AF \_ INET6** e il  parametro di tipo **è \_ RAW** o Unspecified.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | Protocollo PGM per il multicast affidabile. Si tratta di un valore possibile quando il parametro *AF* è **AF \_ inet** e il parametro di *tipo* è **Sock \_ RDM**. Questo protocollo è denominato anche **IPPROTO \_ PGM**. <br/> Questo valore del *protocollo* è supportato solo se è installato il protocollo multicast affidabile.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

ID di processo effettivo o indicatore se l'evento è risultato di un codice Winsock eseguito in un processo di sistema o in un contesto di chiamata di procedura posticipata (DPC) (contesti all'esterno del processo utente).

</dd> <dt>

*Status* 
</dt> <dd>

Codice NTSTATUS per l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento di **\_ \_ creazione evento AFD** viene tracciato per un'operazione di rete Winsock per la creazione di un socket. Il canale per questo evento è Winsock-AFD. Il livello per questo evento è informativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_descrittore evento**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


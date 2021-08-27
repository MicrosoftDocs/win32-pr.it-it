---
description: Evento di traccia di rete Winsock per un'operazione di creazione di socket.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE evento
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
ms.openlocfilehash: 7ae6f50646ad863be711ab6d48e775aeac9023a053e29044f3921e1dee8c9948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121481"
---
# <a name="afd_event_create-event"></a>Evento AFD \_ EVENT \_ CREATE

**L'evento AFD \_ EVENT \_ CREATE** è un evento di traccia di rete Winsock per un'operazione di creazione di socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informazioni su questo evento.

Nella tabella seguente sono elencati i valori possibili per il *parametro EnterExit:*



| Valore                                                                        | Significato                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inizio di una richiesta Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Richiesta Winsock completata.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Il driver Winsock AFD ha seguito un'azione interna (ad esempio, l'interruzione di una connessione).<br/>      |
| <dl> <dt>3</dt> </dl> | Il driver TCP/IP ha causato il verificarsi di questo evento. Ciò indica in genere una notifica dei dati.<br/> |
| <dl> <dt>4</dt> </dl> | Il driver Winsock AFD ha causato il verificarsi di questo evento (ad esempio, l'impostazione di un'opzione socket).<br/> |



 

</dd> <dt>

*Posizione* 
</dt> <dd>

Campo privato usato internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

Indirizzo [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del processo proprietario del socket correlato. Si tratta di una struttura opaca che funge da oggetto processo per un processo. Per altre informazioni, vedere la documentazione Windows Driver Kit per la [struttura EPROCESS.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Endpoint* 
</dt> <dd>

Indirizzo ENDPOINT AFD \_ del socket.

</dd> <dt>

*Addressfamily* 
</dt> <dd>

Specifica della famiglia di indirizzi per il socket. I valori possibili per la famiglia di indirizzi sono definiti nel file di intestazione *Ws2def.h.* Si noti che il file di intestazione *Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

I valori attualmente supportati sono AF INET o AF INET6, ovvero i formati della famiglia di indirizzi \_ \_ Internet per IPv4 e IPv6. Altre opzioni per la famiglia di indirizzi (AD NETBIOS per l'uso con NetBIOS, ad esempio) sono supportate se è installato un provider di servizi Windows Sockets per la famiglia \_ di indirizzi.

La tabella seguente elenca i valori comuni per la famiglia di indirizzi anche se sono possibili molti altri valori.



| Af                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ UNSPEC**</dt> <dt>0</dt> </dl>           | La famiglia di indirizzi non è specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Famiglia protocollo IP versione 4 di indirizzi (IPv4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Famiglia di indirizzi IPX/SPX. Questa famiglia di indirizzi è supportata solo se è installato il protocollo NWLink IPX/SPX NetBIOS Compatible Transport. <br/> Questa famiglia di indirizzi non è supportata in Windows Vista e versioni successive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Famiglia di indirizzi AppleTalk. Questa famiglia di indirizzi è supportata solo se è installato il protocollo AppleTalk. <br/> Questa famiglia di indirizzi non è supportata in Windows Vista e versioni successive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | Famiglia di indirizzi NetBIOS. Questa famiglia di indirizzi è supportata solo se è installato il provider Windows Sockets per NetBIOS. <br/> Il provider Windows Sockets per NetBIOS è supportato nelle versioni a 32 bit di Windows. Questo provider viene installato per impostazione predefinita nelle versioni a 32 bit Windows. <br/> Il provider Windows Sockets per NetBIOS non è supportato nelle versioni a 64 bit di Windows. <br/> Il provider Windows Sockets per NetBIOS supporta solo i socket in cui il parametro *type* è impostato su **SOCK \_ DGRAM.**<br/> Il provider Windows Sockets per NetBIOS non è direttamente correlato [all'interfaccia di programmazione NetBIOS.](/previous-versions/windows/desktop/netbios/portal) L'interfaccia di programmazione NetBIOS non è supportata in Windows Vista, Windows Server 2008 e versioni successive.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | Famiglia di indirizzi IPv6 (Internet Protocol versione 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | Famiglia di indirizzi Infrared Data Association (IrDA). <br/> Questa famiglia di indirizzi è supportata solo se nel computer sono installati una porta a raggi infrarossi e un driver.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Famiglia Bluetooth indirizzi. <br/> Questa famiglia di indirizzi è supportata solo se nel computer sono installati un adattatore Bluetooth e un driver.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*Sockettype* 
</dt> <dd>

Specifica del tipo per il nuovo socket. I valori possibili per il tipo di socket sono definiti nel file *di intestazione Winsock2.h.*

Nella tabella seguente sono elencati i valori possibili per il *parametro di* tipo supportato per Windows Sockets 2:



| Type                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**SOCK \_ FLUSSO**</dt> <dt>1</dt> </dl>          | Tipo di socket che fornisce flussi di byte sequenziati, affidabili, bidirevi basati sulla connessione con un meccanismo di trasmissione dei dati OOB. Questo tipo di socket usa Transmission Control Protocol (TCP) per la famiglia di indirizzi Internet (AF \_ INET o AF \_ INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**SOCK \_ DGRAM**</dt> <dt>2</dt> </dl>             | Tipo di socket che supporta datagrammi, ovvero buffer senza connessione e inaffidabili di una lunghezza massima fissa (in genere piccola). Questo tipo di socket usa il protocollo UDP (User Datagram Protocol) per la famiglia di indirizzi Internet (AF \_ INET o AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**SOCK \_ RAW**</dt> <dt>3</dt> </dl>                   | Tipo di socket che fornisce un socket non elaborato che consente a un'applicazione di modificare la successiva intestazione del protocollo di livello superiore. Per modificare l'intestazione IPv4, è necessario impostare l'opzione socket [**\_ HDRINCL IP**](ipproto-ip-socket-options.md) sul socket. Per modificare l'intestazione IPv6, è necessario impostare [**l'opzione socket \_ IPV6 HDRINCL**](ipproto-ipv6-socket-options.md) nel socket. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**SOCK \_ RDM**</dt> <dt>4</dt> </dl>                   | Tipo di socket che fornisce un datagramma di messaggi affidabile. Un esempio di questo tipo è l'implementazione del protocollo multicast Pragma General Multicast (PGM) in Windows, spesso definita [programmazione multicast affidabile.](reliable-multicast-programming--pgm-.md) <br/> Questo *valore* di tipo è supportato solo se è installato Reliable Multicast Protocol.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**SOCK \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Tipo di socket che fornisce un pacchetto pseudo-flusso basato su datagrammi. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocollo* 
</dt> <dd>

Protocollo da utilizzare. Le opzioni possibili per il *parametro di* protocollo sono specifiche della famiglia di indirizzi e del tipo di socket specificati. I valori possibili *per il* protocollo sono definiti nel file di intestazione *Wsrm.h* e nel tipo di **enumerazione IPPROTO** definito nel file di intestazione *Ws2def.h.* Si noti che il file di intestazione *Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

Se viene specificato il valore 0, il chiamante non vuole specificare un protocollo e il provider di servizi sceglierà *il* protocollo da usare.

La tabella seguente elenca i valori comuni per il *protocollo* anche se sono possibili molti altri valori.



| protocol                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Oggetto Internet Control Message Protocol (ICMP). Si tratta di un valore possibile quando il  parametro *af* è AF **\_ UNSPEC,** AF INET o AF **\_ INET6** e il parametro di tipo è **SOCK \_ RAW** o non specificato. **\_**<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | Oggetto Internet Group Management Protocol (IGMP). Si tratta di un valore possibile quando il  parametro *af* è AF **\_ UNSPEC,** AF INET o AF **\_ INET6** e il parametro di tipo è **SOCK \_ RAW** o non specificato. **\_**<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | Protocollo Bluetooth RADIO Frequency Communications (Bluetooth RFCOMM). Si tratta di un valore possibile quando il *parametro af* è **AF \_ BTH** e il *parametro di* tipo è **SOCK \_ STREAM.** <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | La Transmission Control Protocol (TCP). Si tratta di un valore possibile quando il *parametro af* è **AF \_ INET** o **AF \_ INET6** e il parametro *di* tipo è **SOCK \_ STREAM.**<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Protocollo UDP (User Datagram Protocol). Si tratta di un valore possibile quando il *parametro af* è **AF \_ INET** o **AF \_ INET6** e il parametro *di* tipo è **SOCK \_ DGRAM**.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | Il Internet Control Message Protocol versione 6 (ICMPv6). Si tratta di un valore possibile quando il  parametro *af* è AF **\_ UNSPEC,** AF INET o AF **\_ INET6** e il parametro di tipo è **SOCK \_ RAW** o non specificato. **\_**<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | Protocollo PGM per il multicast affidabile. Si tratta di un valore possibile quando il *parametro af* è **AF \_ INET** e il *parametro di* tipo è **SOCK \_ RDM**. Questo protocollo è denominato **anche IPPROTO \_ PGM.** <br/> Questo *valore* di protocollo è supportato solo se è installato il protocollo Reliable Multicast.<br/> |



 

</dd> <dt>

*Processid* 
</dt> <dd>

ID del processo effettivo o indicatore se l'evento è il risultato dell'esecuzione di codice Winsock in un processo di sistema o in un contesto di chiamata di procedura posticipata (contesti esterni al processo utente).

</dd> <dt>

*Status* 
</dt> <dd>

Codice NTSTATUS per l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'evento AFD \_ EVENT \_ CREATE** viene tracciato per un'operazione di rete Winsock per creare un socket. Il canale per questo evento è Winsock-AFD. Il livello di questo evento è informativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della traccia winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**DESCRITTORE \_ DI EVENTI**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli traccia modifiche catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


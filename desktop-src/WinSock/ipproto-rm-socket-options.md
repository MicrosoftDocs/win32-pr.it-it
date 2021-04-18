---
description: La tabella seguente descrive le \_ Opzioni del socket IPPROTO RM applicabili ai socket creati per la famiglia di indirizzi IPv4 (AF \_ inet) con il parametro Protocol per la funzione Socket specificata come Reliable Multicast (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: Opzioni di IPPROTO_RM socket (gestione e gestione risorse. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327134"
---
# <a name="ipproto_rm-socket-options"></a>\_Opzioni socket IPPROTO RM

La tabella seguente descrive le opzioni del socket **IPPROTO \_ RM** applicabili ai socket creati per la famiglia di indirizzi IPv4 (AF \_ inet) con il parametro *Protocol* per la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) specificata come Reliable Multicast (IPPROTO \_ RM). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

**Windows XP:** La programmazione del multicast affidabile (PGM) non è supportata.

Alcune opzioni del socket richiedono una spiegazione più che queste tabelle possono comportare; tali opzioni contengono collegamenti ad altre pagine.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**\_Opzioni socket IPPROTO RM**</dt> <dd> <dl> <dt> 

| Opzione                              | Recupero | Set | Tipo optVal                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ Aggiungi \_ ricezione \_ se                |     | sì | ULONG                                            | Solo ricevitore. Aggiunge un'interfaccia su cui restare in attesa (il valore predefinito è la prima interfaccia locale enumerata). Il parametro optVal specifica l'interfaccia di rete nell'ordine dei byte di rete da aggiungere. Il valore specificato sostituisce l'interfaccia predefinita alla prima chiamata per un socket specificato e aggiunge altre interfacce nelle chiamate successive. Per ottenere \_ un comportamento inaddr, ogni interfaccia di rete deve essere aggiunta separatamente. |
| RM \_ del \_ Receive \_ se                |     | sì | ULONG                                            | Solo ricevitore. Rimuove un'interfaccia aggiunta tramite RM \_ Aggiungi \_ Receive \_ se. Il parametro optVal specifica l'interfaccia di rete nell'ordine dei byte di rete da eliminare.                                                                                                                                                                                                                                                            |
| \_FlushCache RM                      |     | sì | N/D                                              | Non implementato.                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_opt per Intranet ad alta \_ velocità \_ \_      | sì | sì | ULONG                                            | Solo ricevitore. Specifica se viene utilizzata una connessione LAN a larghezza di banda elevata.                                                                                                                                                                                                                                                                                                                                   |
| \_LATEJOIN RM                        | sì | sì | ULONG                                            | Solo mittente. Percentuale della dimensione della finestra che può essere richiesta dai ricevitori che si uniscono in ritardo all'accettazione della sessione. Il valore massimo è 75% (il valore predefinito è zero). Disabilitare questa impostazione chiamando di nuovo il valore impostato su zero.                                                                                                                                                                                                |
| \_dimensioni della \_ finestra \_ velocità RM              | sì | sì | [**\_finestra di invio RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Solo mittente. Imposta il limite di velocità di trasmissione, il tempo di anticipo della finestra e le dimensioni della finestra.                                                                                                                                                                                                                                                                                                                                   |
| \_statistiche ricevitore \_ RM            | sì |     | [**\_statistiche ricevitore \_ RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Solo ricevitore. Recupera le statistiche per la sessione di ricezione.                                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ frequenza ADV della finestra di trasmissione RM \_ \_         | sì | sì | ULONG                                            | Solo mittente. Specifica la frequenza di avanzamento incrementale per la finestra di invio del bordo finale (il valore predefinito è 15%). Il valore massimo è 50%.                                                                                                                                                                                                                                                                                          |
| \_statistiche mittente \_ RM              | sì |     | [**\_statistiche mittente \_ RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Solo mittente. Recupera le statistiche per la sessione di invio.                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ Metodo Advance della finestra mittente RM \_ | sì | sì | ULONG                                            | Solo mittente. Il parametro optVal specifica il metodo utilizzato per l'avanzamento della finestra di invio del bordo finale. Il parametro optVal può essere impostato solo \_ \_ su E la finestra avanza \_ per \_ ora (impostazione predefinita). Si noti che \_ l' \_ uso \_ della finestra E come \_ cache dei dati \_ non è supportato.                                                                                                                                                                     |
| RM \_ impostare \_ mcast \_ TTL                 |     | sì | ULONG                                            | Solo mittente. Imposta l'impostazione TTL (time to Live) massima per i pacchetti multicast. Il valore massimo e il valore predefinito è 255.                                                                                                                                                                                                                                                                                                      |
| \_ \_ limite messaggi set \_ RM          |     | sì | ULONG                                            | Solo mittente. Specifica le dimensioni del messaggio successivo da inviare, in byte. Significativo solo per i socket in modalità messaggio (SOCK \_ RDM). È possibile impostare mentre è in corso la sessione.                                                                                                                                                                                                                                                |
| RM \_ impostare \_ Invia \_ se                   | sì | sì | ULONG                                            | Solo mittente. Imposta l'indirizzo IP dell'interfaccia mittente nell'ordine dei byte di rete.                                                                                                                                                                                                                                                                                                                                              |
| \_usare \_ FEC per RM                        | sì | sì | [**\_informazioni sul FEC di RM \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Solo mittente. Notifica al mittente di applicare le tecniche di correzione degli errori per inviare i dati di ripristino. FEC presenta tre modalità: solo pacchetti di parità pro-attivo, solo pacchetti di parità OnDemand o entrambi. Per ulteriori informazioni, vedere la struttura delle [**\_ \_ informazioni su RM FEC**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) .                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Supporto di Windows per le opzioni di IPPROTO \_ RM**</dt> <dd> <dl> <dt> 

| Opzione                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ Aggiungi \_ ricezione \_ se                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ del \_ Receive \_ se                | x         | x                   | x             | x                   | x          |              |             |               |
| \_FlushCache RM                      | x         | x                   | x             | x                   | x          |              |             |               |
| \_opt per Intranet ad alta \_ velocità \_ \_      | x         | x                   | x             | x                   | x          |              |             |               |
| \_LATEJOIN RM                        | x         | x                   | x             | x                   | x          |              |             |               |
| \_dimensioni della \_ finestra \_ velocità RM              | x         | x                   | x             | x                   | x          |              |             |               |
| \_statistiche ricevitore \_ RM            | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ frequenza ADV della finestra di trasmissione RM \_ \_         | x         | x                   | x             | x                   | x          |              |             |               |
| \_statistiche mittente \_ RM              | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ \_ Metodo Advance della finestra mittente RM \_ | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ impostare \_ mcast \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ limite messaggi set \_ RM          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ impostare \_ Invia \_ se                   | x         | x                   | x             | x                   | x          |              |             |               |
| \_usare \_ FEC per RM                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **IPPROTO \_ RM** e le strutture usate da queste opzioni del socket sono definite nel file di intestazione di gestione risorse di gestione. *h* .

La **costante \_ IPPROTO RM** o **IPPROTO \_ PGM** può essere usata per specificare il parametro del *protocollo* per la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) per usare le opzioni del socket RM. In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, la **costante \_ IPPROTO PGM** viene definita nel file di intestazione *Ws2def. h* sullo stesso valore della costante **IPPROTO \_ RM** definita nel file di intestazione di gestione risorse di Windows. *h* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gestione risorse di gestione</dt> </dl> |



 

 





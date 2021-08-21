---
description: La tabella seguente descrive le opzioni del socket RM IPPROTO che si applicano ai socket creati per la famiglia di indirizzi IPv4 (AF INET) con il parametro del protocollo per la funzione socket specificata come \_ \_ reliable multicast (IPPROTO \_ RM).
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: IPPROTO_RM Socket Options (Wsrm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1710b1135d2c645f5ff55de12b2feb2d62cfbe2b257e3f28367a66a81d5171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051489"
---
# <a name="ipproto_rm-socket-options"></a>Opzioni socket RM IPPROTO \_

La tabella seguente descrive le opzioni del socket **\_ RM IPPROTO** che si applicano ai socket creati per la famiglia di indirizzi IPv4 (AF INET) con il parametro del protocollo per la funzione socket specificata come \_ reliable multicast (IPPROTO  [](/windows/desktop/api/Winsock2/nf-winsock2-socket) \_ RM). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

**Windows XP:** Reliable Multicast Programming (PGM) non è supportato.

Alcune opzioni socket richiedono una spiegazione maggiore di quanto possano comunicare queste tabelle. Tali opzioni contengono collegamenti a pagine aggiuntive.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Opzioni socket RM IPPROTO \_**</dt> <dd> <dl> <dt> 

| Opzione                              | Recupero | Impostazione | Tipo Optval                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ ADD \_ RECEIVE \_ IF                |     | sì | ULONG                                            | Solo ricevitore. Aggiunge un'interfaccia su cui restare in ascolto (il valore predefinito è la prima interfaccia locale enumerata). Il parametro optval specifica l'interfaccia di rete nell'ordine dei byte di rete da aggiungere. Il valore specificato sostituisce l'interfaccia predefinita alla prima chiamata per un determinato socket e aggiunge altre interfacce nelle chiamate successive. Per ottenere il comportamento INADDR \_ ANY, ogni interfaccia di rete deve essere aggiunta separatamente. |
| RM \_ DEL \_ RECEIVE \_ IF                |     | sì | ULONG                                            | Solo ricevitore. Rimuove un'interfaccia aggiunta tramite RM \_ ADD \_ RECEIVE \_ IF. Il parametro optval specifica l'interfaccia di rete nell'ordine dei byte di rete da eliminare.                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | sì | N/A                                              | Non implementato.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | sì | sì | ULONG                                            | Solo ricevitore. Specifica se viene usata una connessione LAN a larghezza di banda elevata (100 Mbps+).                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | sì | sì | ULONG                                            | Solo mittente. Percentuale delle dimensioni della finestra che possono essere richieste dai ricevitori ad aggiunta tardiva all'accettazione della sessione. Il valore massimo è 75% (il valore predefinito è zero). Disabilitare questa impostazione chiamando di nuovo con il valore impostato su zero.                                                                                                                                                                                                |
| DIMENSIONI DELLA \_ FINESTRA \_ FREQUENZA \_ RM              | sì | sì | [**FINESTRA DI \_ INVIO \_ RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Solo mittente. Imposta il limite di velocità di trasmissione, il tempo di avanzamento della finestra e le dimensioni della finestra.                                                                                                                                                                                                                                                                                                                                   |
| STATISTICHE \_ RICEVITORE \_ RM            | sì |     | [**STATISTICHE \_ \_ RICEVITORE RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Solo ricevitore. Recupera le statistiche per la sessione ricevente.                                                                                                                                                                                                                                                                                                                                                         |
| FREQUENZA \_ \_ ADV DELLA \_ FINESTRA DI INVIO \_ RM         | sì | sì | ULONG                                            | Solo mittente. Specifica la frequenza di avanzamento incrementale per la finestra di invio edge finale (il valore predefinito è 15%). Il valore massimo è 50%.                                                                                                                                                                                                                                                                                          |
| STATISTICHE RM \_ MITTENTE \_              | sì |     | [**STATISTICHE RM \_ \_ MITTENTE**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Solo mittente. Recupera le statistiche per la sessione di invio.                                                                                                                                                                                                                                                                                                                                                             |
| METODO ADVANCE \_ DELLA \_ FINESTRA MITTENTE \_ \_ RM | sì | sì | ULONG                                            | Solo mittente. Il parametro optval specifica il metodo usato per far avanzare la finestra di invio perimetrale finale. Il parametro optval può essere solo E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (impostazione predefinita). Si noti che E \_ WINDOW USE AS DATA CACHE non è \_ \_ \_ \_ supportato.                                                                                                                                                                     |
| RM \_ SET \_ MCAST \_ TTL                 |     | sì | ULONG                                            | Solo mittente. Imposta l'impostazione TTL (Maximum Time To Live) per i pacchetti multicast. Il valore massimo e predefinito è 255.                                                                                                                                                                                                                                                                                                      |
| LIMITE DEL \_ MESSAGGIO RM SET \_ \_          |     | sì | ULONG                                            | Solo mittente. Specifica le dimensioni del messaggio successivo da inviare, in byte. Significativo solo per i socket in modalità messaggio (SOCK \_ RDM). Può essere impostato mentre la sessione è in corso.                                                                                                                                                                                                                                                |
| RM \_ SET \_ SEND \_ IF                   | sì | sì | ULONG                                            | Solo mittente. Imposta l'indirizzo IP dell'interfaccia di invio nell'ordine dei byte di rete.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ USE \_ FEC                        | sì | sì | [**RM \_ FEC \_ INFO**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Solo mittente. Notifica al mittente di applicare tecniche di correzione degli errori di inoltro per inviare i dati di ripristino. FeC ha tre modalità: solo pacchetti di parità pro-attivo, solo pacchetti di parità OnDemand o entrambi. Per [**altre informazioni, vedere Struttura \_ di RM FEC \_ INFO.**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows Supporto per le opzioni RM IPPROTO \_**</dt> <dd> <dl> <dt> 

| Opzione                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ ADD \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ DEL \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| DIMENSIONI DELLA \_ FINESTRA \_ FREQUENZA \_ RM              | x         | x                   | x             | x                   | x          |              |             |               |
| STATISTICHE \_ RICEVITORE \_ RM            | x         | x                   | x             | x                   | x          |              |             |               |
| FREQUENZA \_ \_ ADV DELLA \_ FINESTRA DI INVIO \_ RM         | x         | x                   | x             | x                   | x          |              |             |               |
| STATISTICHE RM \_ MITTENTE \_              | x         | x                   | x             | x                   | x          |              |             |               |
| METODO ADVANCE \_ DELLA \_ FINESTRA MITTENTE \_ \_ RM | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| LIMITE DEL \_ MESSAGGIO RM SET \_ \_          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ SEND \_ IF                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ USE \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ RM IPPROTO** e le strutture usate da queste opzioni di socket sono definite nel file *di intestazione Wsrm.h.*

La **costante IPPROTO \_ RM** o **IPPROTO \_ PGM**  può essere usata per specificare il parametro di protocollo per la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) per usare le opzioni socket RM. In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, la costante **IPPROTO \_ PGM** viene definita nel file di intestazione *Ws2def.h* allo stesso valore della costante **IPPROTO \_ RM** definita nel file di intestazione *Wsrm.h.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wsrm.h</dt> </dl> |



 

 





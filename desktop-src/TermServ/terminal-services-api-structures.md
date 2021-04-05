---
title: Strutture API Servizi Desktop remoto
description: Elenca le strutture usate con l'API Servizi Desktop remoto.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117799"
---
# <a name="remote-desktop-services-api-structures"></a>Strutture API Servizi Desktop remoto

Con l'API Servizi Desktop remoto vengono utilizzate le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**\_def canale**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contiene il nome e le opzioni di un canale virtuale Servizi Desktop remoto.

</dd> <dt>

[**\_punti di ingresso del canale \_**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contiene i puntatori alle funzioni chiamate da una DLL sul lato client per accedere ai canali virtuali.

</dd> <dt>

[**\_intestazione PDU del canale \_**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contiene informazioni su un blocco di dati ricevuto dall'entità finale del server di un canale virtuale.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contiene informazioni su una licenza di Servizi Desktop remoto specifica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contiene informazioni su un client Connessione Desktop remoto (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contiene informazioni su una sessione di Servizi Desktop remoto.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contiene informazioni su una sessione di Servizi Desktop remoto.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contiene un'Unione a [**\_ livello di WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) che contiene informazioni estese su una sessione di Servizi Desktop remoto.

</dd> <dt>

[**\_Level1 WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contiene informazioni estese su una sessione di Servizi Desktop remoto.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contiene informazioni su un listener di Servizi Desktop remoto.

</dd> <dt>

[**\_indirizzo IP \_ WTSSBX**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contiene informazioni sull'indirizzo IP di una risorsa di rete.

</dd> <dt>

[**\_informazioni sulla \_ connessione del computer WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contiene informazioni su un computer che accetta connessioni remote.

</dd> <dt>

[**\_informazioni sul computer WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contiene informazioni su un computer e il relativo stato corrente.

</dd> <dt>

[**\_informazioni sulla sessione WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Sono incluse informazioni sulle sessioni disponibili per Connessione Desktop remoto broker (gestore connessione Desktop remoto).

</dd> <dt>

[**\_notifica WTSSESSION**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Fornisce informazioni sulla notifica di modifica della sessione. Un servizio riceve questa struttura nella relativa funzione [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) in risposta a un evento di modifica della sessione.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contiene le informazioni di configurazione per un utente in un controller di dominio o in un server di host sessione Desktop remoto (host sessione Desktop remoto).

</dd> <dt>

[**\_Indirizzo client \_ WTS**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contiene l'indirizzo di rete del client di una sessione di Servizi Desktop remoto.

</dd> <dt>

[**\_visualizzazione client \_ WTS**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contiene informazioni sulla visualizzazione di un client Connessione Desktop remoto (RDC).

</dd> <dt>

[**\_informazioni sul processo WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contiene informazioni su un processo in esecuzione in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_informazioni sul processo WTS \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contiene informazioni estese su un processo in esecuzione in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_informazioni sul prodotto WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Dettagli della licenza del prodotto necessaria per la connessione a un server terminal.

</dd> <dt>

[**\_informazioni sul server WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contiene informazioni su un server di Servizi Desktop remoto specifico.

</dd> <dt>

[**\_indirizzo della sessione WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contiene l'indirizzo IP virtuale assegnato a una sessione.

</dd> <dt>

[**\_informazioni sulla sessione WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contiene informazioni su una sessione client in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_Informazioni sulla sessione WTS \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contiene informazioni estese su una sessione client in un server Host sessione Desktop remoto o in un server Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).

</dd> </dl>

 

 
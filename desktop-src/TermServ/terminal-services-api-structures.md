---
title: Servizi Desktop remoto di API
description: Elenca le strutture usate con l'API Servizi Desktop remoto.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000101"
---
# <a name="remote-desktop-services-api-structures"></a>Servizi Desktop remoto di API

Le strutture seguenti vengono usate con l'API Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**DEF \_ DEL CANALE**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contiene il nome e le opzioni di un Servizi Desktop remoto virtuale.

</dd> <dt>

[**PUNTI \_ DI INGRESSO DEL \_ CANALE**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contiene puntatori alle funzioni chiamate da una DLL sul lato client per accedere ai canali virtuali.

</dd> <dt>

[**INTESTAZIONE \_ PDU \_ DEL CANALE**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contiene informazioni su un blocco di dati ricevuto dall'estremità del server di un canale virtuale.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contiene informazioni su un key pack specifico Servizi Desktop remoto licenze.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contiene informazioni su una licenza Servizi Desktop remoto specifica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contiene informazioni su un client Connessione Desktop remoto (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contiene informazioni su una Servizi Desktop remoto sessione.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contiene informazioni su una Servizi Desktop remoto sessione.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contiene [**un'unione WTSINFOEX \_ LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) che contiene informazioni estese su una Servizi Desktop remoto sessione.

</dd> <dt>

[**WTSINFOEX \_ LEVEL1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contiene informazioni estese su una Servizi Desktop remoto sessione.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contiene informazioni su un listener Servizi Desktop remoto di dati.

</dd> <dt>

[**INDIRIZZO IP WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contiene informazioni sull'indirizzo IP di una risorsa di rete.

</dd> <dt>

[**WTSSBX \_ MACHINE \_ CONNECT \_ INFO**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contiene informazioni su un computer che accetta connessioni remote.

</dd> <dt>

[**INFORMAZIONI SUL COMPUTER WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contiene informazioni su un computer e sul relativo stato corrente.

</dd> <dt>

[**INFORMAZIONI SULLA SESSIONE WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contiene informazioni sulle sessioni disponibili per Connessione Desktop remoto Broker (Gestore connessione Desktop remoto).

</dd> <dt>

[**NOTIFICA \_ WTSSESSION**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Fornisce informazioni sulla notifica di modifica della sessione. Un servizio riceve questa struttura nella relativa [*funzione HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) in risposta a un evento di modifica della sessione.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contiene informazioni di configurazione per un utente in un controller di dominio o Desktop remoto host sessione Desktop remoto.

</dd> <dt>

[**\_WTS INDIRIZZO \_ CLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contiene l'indirizzo di rete client di una Servizi Desktop remoto sessione.

</dd> <dt>

[**\_WTS VISUALIZZAZIONE \_ CLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contiene informazioni sulla visualizzazione di un client Connessione Desktop remoto (RDC).

</dd> <dt>

[**\_WTS INFORMAZIONI SUL \_ PROCESSO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contiene informazioni su un processo in esecuzione in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_WTS INFORMAZIONI \_ SUL \_ PROCESSO EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contiene informazioni estese su un processo in esecuzione in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_WTS INFORMAZIONI SUL \_ PRODOTTO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Dettagli della licenza del prodotto necessaria per connettersi a un server terminal.

</dd> <dt>

[**\_WTS INFORMAZIONI \_ SERVER**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contiene informazioni su un server Servizi Desktop remoto specifico.

</dd> <dt>

[**\_WTS INDIRIZZO \_ DI SESSIONE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contiene l'indirizzo IP virtuale assegnato a una sessione.

</dd> <dt>

[**\_WTS INFORMAZIONI SULLA \_ SESSIONE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contiene informazioni su una sessione client in un server Host sessione Desktop remoto.

</dd> <dt>

[**\_WTS INFORMAZIONI \_ SULLA \_ SESSIONE 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contiene informazioni estese su una sessione client in un server Host sessione Desktop remoto o Desktop remoto server Host di virtualizzazione Desktop remoto.

</dd> </dl>

 

 
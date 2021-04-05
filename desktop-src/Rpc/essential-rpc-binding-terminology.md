---
title: Terminologia di associazione RPC essenziale
description: Per semplificare la discussione del processo di connessione client/server, è utile comprendere i termini seguenti.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- RPC (Remote Procedure Call) RPC, descritta, associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047194"
---
# <a name="essential-rpc-binding-terminology"></a>Terminologia di associazione RPC essenziale

Per semplificare la discussione del processo di connessione client/server, è utile comprendere i termini seguenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Sequenza di protocollo
</dt> <dd>

Quando i sistemi operativi di rete comunicano tra loro, devono restare in ascolto e parlare della stessa lingua. Queste lingue sono denominate *sequenze di protocollo*. I programmi client e server devono usare le sequenze di protocollo supportate dalla rete che li connette. Microsoft RPC supporta un'ampia gamma di sequenze di protocolli. Per informazioni dettagliate, vedere [selezione di una sequenza di protocollo](selecting-a-protocol-sequence.md), [specifica di sequenze di protocollo](specifying-protocol-sequences.md)ed [**endpoint**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Computer host server o sistema host server
</dt> <dd>

Il programma server viene eseguito nel computer host server. Tuttavia, la maggior parte della letteratura sull'elaborazione client/server si riferisce sia al programma server sia al computer host server come "Server". Il risultato è che non è sempre chiaro che verrà discusso.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint
</dt> <dd>

I programmi server restano in attesa di una porta o di un gruppo di porte nel computer host server per le richieste client. I sistemi host server gestiscono un database di queste porte, denominate endpoint in RPC. Il database è denominato mappa dell'endpoint.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Associazione
</dt> <dd>

I programmi client creano un'associazione al server per stabilire una sessione di comunicazione. Un'associazione contiene tutte le informazioni necessarie per la creazione della sessione da parte delle applicazioni client.

</dd> </dl>

 

 
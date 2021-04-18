---
description: Il protocollo di handshake Transport Layer Security (TLS) è responsabile dell'autenticazione e dello scambio di chiave necessari per stabilire o riprendere le sessioni sicure.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocollo handshake TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316204"
---
# <a name="tls-handshake-protocol"></a>Protocollo handshake TLS

Il protocollo di handshake [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) è responsabile dell'autenticazione e dello scambio di chiave necessari per stabilire o riprendere le sessioni sicure. Quando si stabilisce una [*sessione*](../secgloss/s-gly.md)protetta, il protocollo di handshake gestisce quanto segue:

-   Negoziazione del pacchetto di crittografia
-   Autenticazione del server e, facoltativamente, del client
-   Scambio di informazioni sulla chiave della sessione.

## <a name="cipher-suite-negotiation"></a>Negoziazione del pacchetto di crittografia

Il client e il server fanno contatto e scelgono il pacchetto di crittografia che verrà usato durante lo scambio di messaggi.

## <a name="authentication"></a>Authentication

In TLS, un server dimostra la propria identità al client. Il client potrebbe anche dover dimostrare la propria identità al server. L'uso di coppie di [*chiavi pubbliche/private*](../secgloss/p-gly.md)è la base di questa autenticazione. Il metodo esatto utilizzato per l'autenticazione è determinato dal pacchetto di crittografia negoziato.

## <a name="key-exchange"></a>Scambio di chiave

Il client e il server scambiano numeri casuali e un numero speciale denominato master secret. Questi numeri vengono combinati con dati aggiuntivi che consentono a client e server di creare il segreto condiviso, denominato master secret. Il master secret viene utilizzato dal client e dal server per generare il segreto di scrittura, ovvero la chiave della sessione utilizzata per l' [*hashing*](../secgloss/h-gly.md), e la chiave di scrittura, ovvero la [*chiave di sessione*](../secgloss/s-gly.md) utilizzata per la crittografia.

## <a name="establishing-a-secure-session-by-using-tls"></a>Stabilire una sessione protetta usando TLS

Il protocollo di handshake TLS prevede i passaggi seguenti:

1.  Il client invia al server un messaggio "Hello client", insieme al valore casuale del client e ai pacchetti di crittografia supportati.
2.  Il server risponde inviando un messaggio "Server Hello" al client, insieme al valore casuale del server.
3.  Il server invia il certificato al client per l'autenticazione e può richiedere un certificato dal client. Il server invia il messaggio "Server Hello done".
4.  Se il server ha richiesto un certificato dal client, il client lo invierà.
5.  Il client crea un segreto preliminare casuale e lo crittografa con la [*chiave pubblica*](../secgloss/p-gly.md) dal certificato del server, inviando il segreto pre-master crittografato al server.
6.  Il server riceve il segreto pre-master. Il server e il client generano ognuno il master secret e le [*chiavi di sessione*](../secgloss/s-gly.md) in base al master secret.
7.  Il client invia una notifica di "modifica specifica crittografia" al server per indicare che il client inizierà a utilizzare le nuove [*chiavi di sessione*](../secgloss/s-gly.md) per l' [*hashing*](../secgloss/h-gly.md) e la crittografia dei messaggi. Il client invia anche il messaggio "client completato".
8.  Il server riceve "modifica specifica crittografia" e passa lo stato di sicurezza del livello record alla [*crittografia simmetrica*](../secgloss/s-gly.md) usando le [*chiavi di sessione*](../secgloss/s-gly.md). Il server invia il messaggio "Server completato" al client.
9.  Il client e il server possono ora scambiare dati dell'applicazione tramite il canale protetto stabilito. Tutti i messaggi inviati dal client al server e dal server al client vengono crittografati tramite la chiave della sessione.

## <a name="resuming-a-secure-session-by-using-tls"></a>Ripresa di una sessione protetta tramite TLS

1.  Il client invia un messaggio "Hello client" utilizzando l'ID sessione della sessione da riprendere.
2.  Il server controlla la cache della sessione per un ID di sessione corrispondente. Se viene trovata una corrispondenza e il server è in grado di riprendere la sessione, invia un messaggio "Server Hello" con l'ID sessione.
    > [!Note]  
    > Se non viene trovata una corrispondenza con ID di sessione, il server genera un nuovo ID di sessione e il client e il server TLS eseguono un handshake completo.

     

3.  Il client e il server devono scambiare messaggi di "modifica della specifica della crittografia" e inviare i messaggi "client terminato" e "Server completato".
4.  Il client e il server possono ora riprendere lo scambio di dati dell'applicazione sul canale sicuro.

 

 

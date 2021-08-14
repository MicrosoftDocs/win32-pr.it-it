---
description: Il Transport Layer Security (TLS) Handshake Protocol è responsabile dell'autenticazione e dello scambio di chiavi necessario per stabilire o riprendere sessioni protette.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocollo handshake TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe32e11127bf46088aa04e58dd6444620cea327c08d2609e01749efcb1e00df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915819"
---
# <a name="tls-handshake-protocol"></a>Protocollo handshake TLS

Il [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Handshake Protocol è responsabile dell'autenticazione e dello scambio di chiavi necessario per stabilire o riprendere sessioni protette. Quando si stabilisce una sessione [*protetta,*](../secgloss/s-gly.md)il protocollo Handshake gestisce quanto segue:

-   Negoziazione della suite di crittografia
-   Autenticazione del server e, facoltativamente, del client
-   Scambio di informazioni sulle chiavi di sessione.

## <a name="cipher-suite-negotiation"></a>Negoziazione di Cipher Suite

Il client e il server contattano e scelgono la suite di crittografia che verrà usata durante lo scambio di messaggi.

## <a name="authentication"></a>Autenticazione

In TLS, un server dimostra la propria identità al client. Il client potrebbe anche dover dimostrare la propria identità al server. L'infrastruttura a chiave pubblica, l'uso di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md)è alla base di questa autenticazione. Il metodo esatto usato per l'autenticazione è determinato dalla suite di crittografia negoziata.

## <a name="key-exchange"></a>Chiave Exchange

Il client e il server scambiano numeri casuali e un numero speciale denominato Segreto pre-master. Questi numeri vengono combinati con dati aggiuntivi che consente a client e server di creare il segreto condiviso, denominato master secret. Il segreto master viene usato dal client e dal server per generare il segreto MAC di scrittura, [](../secgloss/s-gly.md) ovvero la chiave di sessione usata per [*l'hashing,*](../secgloss/h-gly.md)e la chiave di scrittura, ovvero la chiave di sessione usata per la crittografia.

## <a name="establishing-a-secure-session-by-using-tls"></a>Definizione di una sessione protetta tramite TLS

Il protocollo handshake TLS prevede i passaggi seguenti:

1.  Il client invia un messaggio "Client hello" al server, insieme al valore casuale del client e alle suite di crittografia supportate.
2.  Il server risponde inviando un messaggio "Server hello" al client, insieme al valore casuale del server.
3.  Il server invia il certificato al client per l'autenticazione e può richiedere un certificato al client. Il server invia il messaggio "Server hello done".
4.  Se il server ha richiesto un certificato al client, il client lo invia.
5.  Il client crea un segreto pre-master casuale e lo crittografa con la chiave pubblica dal certificato del server, inviando il segreto pre-master crittografato al server. [](../secgloss/p-gly.md)
6.  Il server riceve il segreto pre-master. Ogni server e client generano il segreto master e le chiavi [*di sessione*](../secgloss/s-gly.md) in base al segreto pre-master.
7.  Il client invia al server la notifica "Modifica specifica di crittografia" per indicare che il client inizierà a usare le nuove chiavi di sessione per l'hashing e la crittografia dei messaggi. [](../secgloss/s-gly.md) [](../secgloss/h-gly.md) Il client invia anche il messaggio "Client completato".
8.  Il server riceve la "modifica della specifica di crittografia" e passa lo stato di sicurezza del livello di record alla crittografia [*simmetrica*](../secgloss/s-gly.md) usando le [*chiavi di sessione*](../secgloss/s-gly.md). Il server invia il messaggio "Server completato" al client.
9.  Il client e il server possono ora scambiare i dati dell'applicazione tramite il canale protetto stabilito. Tutti i messaggi inviati dal client al server e dal server al client vengono crittografati usando la chiave di sessione.

## <a name="resuming-a-secure-session-by-using-tls"></a>Ripresa di una sessione protetta tramite TLS

1.  Il client invia un messaggio "Client hello" usando l'ID sessione della sessione da riprendere.
2.  Il server verifica la presenza di un ID sessione corrispondente nella cache di sessione. Se viene trovata una corrispondenza e il server è in grado di riprendere la sessione, invia un messaggio "Server hello" con l'ID sessione.
    > [!Note]  
    > Se non viene trovata una corrispondenza di ID sessione, il server genera un nuovo ID sessione e il client TLS e il server eseguono un handshake completo.

     

3.  Client e server devono scambiare messaggi "Modifica specifica di crittografia" e inviare messaggi "Client completato" e "Server completato".
4.  Il client e il server possono ora riprendere lo scambio di dati dell'applicazione tramite il canale protetto.

 

 

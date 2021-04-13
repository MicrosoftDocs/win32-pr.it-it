---
description: Esempio di scambio di pacchetti di protocollo SMB Microsoft tra un client e un server.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: Scenario di scambio di pacchetti del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a03e2f75b00aa93e629b3e698631c5efde4694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343191"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>Scenario di scambio di pacchetti del protocollo SMB Microsoft

Questo argomento fornisce un esempio di scambio di pacchetti di protocollo SMB Microsoft tra un client e un server. I passaggi seguenti sono una panoramica del processo:

1.  Il client e il server stabiliscono una sessione NetBIOS.
2.  Il client e il server negoziano il dialetto del protocollo SMB Microsoft.
3.  Il client accede al server.
4.  Il client si connette a una condivisione sul server.
5.  Il client apre un file nella condivisione.
6.  Il client legge dal file.

In primo luogo, una connessione TCP full-duplex viene stabilita dal client con il server. Quindi, il client compila e invia un pacchetto di richiesta di sessione NetBIOS sulla connessione TCP. Se il pacchetto è stato formattato correttamente, il server restituisce un pacchetto contenente un messaggio che conferma che la sessione è stata stabilita. Al termine di questa operazione, il client invia al server i pacchetti del primo protocollo SMB Microsoft.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pacchetto 1: \_ negoziazione com \_ SMB**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede che il server negozi il sottolinguaggio del protocollo SMB Microsoft. Un elenco di stringhe che identificano i dialetti con cui il client può lavorare è incluso nel pacchetto.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Pacchetto 2: \_ negoziazione com \_ SMB**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Il server risponde alla richiesta del client di identificare il dialetto del protocollo SMB Microsoft che verrà usato nella sessione. Il pacchetto restituito include anche una stringa casuale a 8 byte che verrà usata nel passaggio successivo per autenticare il client durante il processo di accesso.<br/>                                                                                                                                                                                                                                   |
| **Pacchetto 3: \_ configurazione della \_ sessione com SMB \_ \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Questo pacchetto include informazioni sulle funzionalità client, quindi questo pacchetto deve essere inviato anche se il server ha implementato solo la sicurezza a livello di condivisione.<br/> **Pacchetto 3: \_ configurazione della \_ sessione com SMB \_ \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se la richiesta di verifica/risposta viene accettata dal server, nel pacchetto restituito al client viene incluso un UID valido. Se non viene accettato, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso.<br/> |
| **Pacchetto 4: \_ albero com \_ SMB \_ Connect \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede l'accesso alla condivisione. Il pacchetto contiene il percorso della condivisione completamente specificato in formato UNC.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Pacchetto 5: \_ albero com \_ SMB \_ Connect \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se viene concesso l'accesso alla condivisione, il server restituisce l'ID di albero a 16 bit (TID) che corrisponde alla condivisione in questo pacchetto. Se la condivisione non esiste o l'utente non dispone di credenziali sufficienti per accedere alla condivisione, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso alla condivisione.<br/>                                                                                                                                                                                                 |
| **Pacchetto 6: SMB \_ com \_ aperto \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede al server di aprire un file nella condivisione a cui si accede per conto del client. Questo pacchetto contiene il nome del file da aprire.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Pacchetto 7: SMB \_ com \_ aperto \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se viene concesso l'accesso al file, il server restituisce l'ID del file richiesto. Se il file non esiste o l'utente non dispone di credenziali sufficienti per accedere al file, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso al file.<br/>                                                                                                                                                                                                                                                  |
| **Pacchetto 8: \_ ANDX di \_ lettura \_ com SMB**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede al server di leggere i dati dal file aperto per conto del client e di restituire i dati al client. L'ID file ottenuto dal client quando il file è stato aperto è incluso in questo pacchetto per identificare il file aperto dal quale il server deve leggere i dati.<br/>                                                                                                                                                                                                                   |
| **Pacchetto 9: \_ ANDX di \_ lettura \_ com SMB**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Il server restituisce i dati dei file richiesti in questo pacchetto. Un errore in questo caso è improbabile dato che è stato concesso l'accesso al server, alla condivisione e al file. Questo può verificarsi in alcune situazioni, tuttavia, ad esempio, se l'accesso a una condivisione viene modificato tra l'ora in cui il file viene aperto e l'ora in cui viene eseguita la lettura.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> Se si implementa un CIFS che non supporta le notifiche delle modifiche, Windows non è in grado di mantenere un handle in attesa per la file system e la connessione SMB può scomparire senza preavviso.

 

 

 





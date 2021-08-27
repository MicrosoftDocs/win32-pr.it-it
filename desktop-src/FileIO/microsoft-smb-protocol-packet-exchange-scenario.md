---
description: Esempio di scambio di pacchetti del protocollo SMB Microsoft tra un client e un server.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: Scenario di gestione dei pacchetti del Exchange Microsoft SMB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47415c6d49f6c1f7b924719d4d012277c03956c1af0d948b3ef66049c1203641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048051"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>Scenario di gestione dei pacchetti del Exchange Microsoft SMB

In questo argomento viene illustrato un esempio di scambio di pacchetti del protocollo SMB Microsoft tra un client e un server. I passaggi seguenti sono una panoramica del processo:

1.  Il client e il server stabiliscono una sessione NetBIOS.
2.  Il client e il server negoziano il dialetto del protocollo Microsoft SMB.
3.  Il client accede al server.
4.  Il client si connette a una condivisione nel server.
5.  Il client apre un file nella condivisione.
6.  Il client legge dal file.

In primo luogo, viene stabilita una connessione TCP full-duplex dal client con il server. Il client compila quindi e invia un pacchetto di richiesta di sessione NetBIOS sulla connessione TCP. Se il pacchetto è stato formattato correttamente, il server restituisce un pacchetto che contiene un messaggio che conferma che la sessione è stata stabilita. Successivamente, il client invia i primi pacchetti del protocollo Microsoft SMB al server.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pacchetto 1: SMB \_ COM \_ NEGOTIATE**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede che il server negozi il dialetto del protocollo Microsoft SMB. Nel pacchetto è incluso un elenco di stringhe che identificano i dialetti che il client può usare.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Pacchetto 2: SMB \_ COM \_ NEGOTIATE**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Il server risponde alla richiesta del client di identificare il dialetto del protocollo Microsoft SMB che verrà usato nella sessione. Il pacchetto restituito include anche una stringa casuale a 8 byte che verrà usata nel passaggio successivo per autenticare il client durante il processo di accesso.<br/>                                                                                                                                                                                                                                   |
| **Pacchetto 3: SMB \_ COM \_ SESSION SETUP \_ \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Questo pacchetto include informazioni sulle funzionalità client, pertanto questo pacchetto deve essere inviato anche se il server ha implementato solo la sicurezza a livello di condivisione.<br/> **Pacchetto 3: SMB \_ COM \_ SESSION SETUP \_ \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se la richiesta di verifica/risposta viene accettata dal server, nel pacchetto restituito al client viene incluso un UID valido. Se non viene accettato, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso.<br/> |
| **Pacchetto 4: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede l'accesso alla condivisione. Il pacchetto contiene il percorso completo specificato della condivisione in formato UNC.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Pacchetto 5: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se viene concesso l'accesso alla condivisione, il server restituisce l'ID albero a 16 bit (TID) corrispondente alla condivisione in questo pacchetto. Se la condivisione non esiste o l'utente non dispone di credenziali sufficienti per accedere alla condivisione, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso alla condivisione.<br/>                                                                                                                                                                                                 |
| **Pacchetto 6: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede al server di aprire un file nella condivisione a cui si accede per conto del client. Questo pacchetto contiene il nome del file da aprire.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Pacchetto 7: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Se viene concesso l'accesso al file, il server restituisce l'ID del file richiesto. Se il file non esiste o se le credenziali dell'utente non sono sufficienti per accedere al file, il server restituirà un codice di errore in questo pacchetto e negherà l'accesso al file.<br/>                                                                                                                                                                                                                                                  |
| **Pacchetto 8: SMB \_ COM \_ READ \_ ANDX**<br/> **Direzione:** Da client a server<br/> **Descrizione:** Il client richiede al server di leggere i dati dal file aperto per conto del client e restituire tali dati al client. L'ID file ottenuto dal client al momento dell'apertura del file è incluso in questo pacchetto per identificare il file aperto da cui il server deve leggere i dati.<br/>                                                                                                                                                                                                                   |
| **Pacchetto 9: SMB \_ COM \_ READ \_ ANDX**<br/> **Direzione:** Da server a client<br/> **Descrizione:** Il server restituisce i dati del file richiesti in questo pacchetto. In questo caso è improbabile che l'accesso al server, alla condivisione e al file sia stato concesso. Può tuttavia verificarsi in alcune situazioni, ad esempio se l'accesso a una condivisione viene modificato tra l'apertura del file e l'ora di lettura.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> Se si implementa un CIFS che non supporta le notifiche di modifica, Windows non può mantenere un handle in attesa per il file system e la connessione SMB può essere inviare senza preavviso.

 

 

 





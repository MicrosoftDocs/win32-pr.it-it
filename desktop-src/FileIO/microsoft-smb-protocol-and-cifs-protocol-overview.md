---
description: Descrive l'implementazione Microsoft del protocollo Server Message Block (SMB).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Panoramica del protocollo SMB Microsoft e del protocollo CIFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09702c719d4e4c5225b35691d7e23980c90c959b7096d7995f3d60b3ef0b204b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951150"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Panoramica del protocollo SMB Microsoft e del protocollo CIFS

Il Server Message Block (SMB) è un protocollo di condivisione file di rete e implementato in Microsoft Windows è noto come protocollo SMB Microsoft. Il set di pacchetti di messaggi che definisce una determinata versione del protocollo è detto dialetto. Il protocollo CIFS (Common Internet File System) è un dialetto di SMB. Sia SMB che CIFS sono disponibili anche nelle macchine virtuali, in diverse versioni di Unix e in altri sistemi operativi.

Il riferimento tecnico a CIFS è disponibile Microsoft Corporation in [Common Internet File System (CIFS) File Access Protocol](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

Anche se lo scopo principale è la condivisione di file, le funzionalità aggiuntive del protocollo Microsoft SMB includono quanto segue:

-   [Negoziazione dialetto](microsoft-smb-protocol-dialects.md)
-   Determinazione di altri server del protocollo Microsoft SMB in rete o esplorazione di rete
-   Stampa in rete
-   [Autenticazione dell'accesso a file, directory e condivisione](microsoft-smb-protocol-authentication.md)
-   Blocco di file e record
-   Notifica di modifica di file e directory
-   Gestione degli attributi di file estesi
-   Supporto Unicode
-   [Blocchi opportunistici](opportunistic-locks.md)

Nel modello di rete OSI, il protocollo Microsoft SMB viene usato più spesso come livello applicazione o protocollo di livello presentazione e si basa su protocolli di livello inferiore per il trasporto. Il protocollo del livello di trasporto con cui viene usato più spesso il protocollo Microsoft SMB è NetBIOS su TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Tuttavia, il protocollo Microsoft SMB può essere usato anche senza un protocollo di trasporto separato, la combinazione Protocollo SMB Microsoft/NBT viene in genere usata per la compatibilità con le versioni precedenti.

Il protocollo Microsoft SMB è un'implementazione client-server ed è costituito da un set di pacchetti di dati, ognuno dei quali contiene una richiesta inviata dal client o una risposta inviata dal server. Questi pacchetti possono essere classificati in modo generale come segue:

-   Pacchetti di controllo sessione Stabilisce e interrompe una connessione alle risorse del server condivise.
-   Pacchetti di accesso ai file Accede e modifica file e directory nel server remoto.
-   Pacchetti di messaggi generali Invia dati a code di stampa, mailslot e named pipe e fornisce dati sullo stato delle code di stampa.

Alcuni pacchetti di messaggi possono essere raggruppati e inviati in una sola trasmissione per ridurre la latenza di risposta e aumentare la larghezza di banda di rete. Questa operazione è denominata "invio in batch". La [sezione Microsoft SMB Protocol Packet Exchange Scenario](microsoft-smb-protocol-packet-exchange-scenario.md) descrive un esempio di sessione del protocollo Microsoft SMB che usa l'invio in batch di pacchetti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialetti del protocollo SMB Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Per stabilire una connessione tra un client e un server usando il protocollo Microsoft SMB, è innanzitutto necessario determinare il dialetto con il massimo livello di funzionalità supportato sia dal client che dal server.<br/>                                                      |
| [Autenticazione del protocollo SMB Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | Il modello di sicurezza usato nel protocollo Microsoft SMB è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di utente e condivisione di sicurezza. Una condivisione è un file, una directory o una stampante accessibile dai client del protocollo Microsoft SMB.<br/> |
| [Scenario di gestione pacchetti Exchange protocollo SMB Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Esempio di scambio di pacchetti del protocollo SMB Microsoft tra un client e un server.<br/>                                                                                                                                                                               |



 

 


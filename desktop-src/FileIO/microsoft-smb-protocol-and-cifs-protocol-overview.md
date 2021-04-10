---
description: Viene descritta l'implementazione Microsoft del protocollo SMB (Server Message Block).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Cenni preliminari sul protocollo Microsoft SMB e sul protocollo CIFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966643"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Cenni preliminari sul protocollo Microsoft SMB e sul protocollo CIFS

Il protocollo SMB (Server Message Block) è un protocollo di condivisione file di rete e, come implementato in Microsoft Windows, è noto come protocollo SMB Microsoft. Il set di pacchetti di messaggi che definisce una particolare versione del protocollo viene definito dialetto. Il protocollo CIFS (Common Internet file System) è un sottolinguaggio SMB. Sia SMB che CIFS sono disponibili anche in macchine virtuali, diverse versioni di UNIX e altri sistemi operativi.

Il riferimento tecnico per CIFS è disponibile da Microsoft Corporation presso il [protocollo di accesso ai file Common Internet file System (CIFS)](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

Sebbene lo scopo principale sia la condivisione di file, la funzionalità del protocollo SMB Microsoft aggiuntiva include quanto segue:

-   [Negoziazione dialetto](microsoft-smb-protocol-dialects.md)
-   Determinazione di altri server del protocollo SMB Microsoft nella rete o esplorazione della rete
-   Stampa su una rete
-   [Autenticazione dell'accesso a file, directory e condivisioni](microsoft-smb-protocol-authentication.md)
-   Blocco di file e record
-   Notifica di modifica di file e directory
-   Gestione degli attributi di file estesi
-   Supporto Unicode
-   [Blocchi opportunistici](opportunistic-locks.md)

Nel modello di rete OSI, il protocollo SMB Microsoft viene usato più spesso come livello dell'applicazione o protocollo di livello di presentazione e si basa su protocolli di livello inferiore per il trasporto. Il protocollo del livello di trasporto con cui il protocollo SMB Microsoft viene usato più spesso è NetBIOS su TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Il protocollo Microsoft SMB, tuttavia, può essere utilizzato anche senza un protocollo di trasporto separato. la combinazione protocollo/NBT Microsoft SMB viene in genere utilizzata per la compatibilità con le versioni precedenti.

Il protocollo Microsoft SMB è un'implementazione client-server ed è costituito da un set di pacchetti di dati, ognuno dei quali contiene una richiesta inviata dal client o una risposta inviata dal server. Questi pacchetti possono essere ampiamente classificati come segue:

-   Pacchetti di controllo della sessione stabilisce e interrompe una connessione alle risorse del server condiviso.
-   I pacchetti di accesso ai file accedono e modificano i file e le directory nel server remoto.
-   I pacchetti di messaggi generali inviano dati a code di stampa, mailslot e named pipe e forniscono dati sullo stato delle code di stampa.

Alcuni pacchetti di messaggi possono essere raggruppati e inviati in una sola trasmissione per ridurre la latenza di risposta e aumentare la larghezza di banda di rete. Questa operazione è denominata "invio in batch". La sezione [scenario di scambio di pacchetti del protocollo SMB Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md) descrive un esempio di sessione del protocollo SMB Microsoft che utilizza l'invio in batch dei pacchetti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialetti del protocollo SMB Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Per stabilire una connessione tra un client e un server utilizzando il protocollo SMB Microsoft, è necessario innanzitutto determinare il dialetto con il livello più elevato di funzionalità supportate dal client e dal server.<br/>                                                      |
| [Autenticazione del protocollo SMB Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | Il modello di sicurezza usato nel protocollo SMB Microsoft è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di utente e condivisione di sicurezza. Una condivisione è un file, una directory o una stampante a cui è possibile accedere dai client del protocollo SMB Microsoft.<br/> |
| [Scenario di scambio di pacchetti del protocollo SMB Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Esempio di scambio di pacchetti di protocollo SMB Microsoft tra un client e un server.<br/>                                                                                                                                                                               |



 

 


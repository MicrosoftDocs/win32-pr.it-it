---
title: Codici di errore Win32
description: Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d8151c07fb6470d395f15e088ae5e50f3e43bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955074"
---
# <a name="win32-error-codes"></a>Codici di errore Win32

Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI.



| Valore di errore ADSI | Messaggio LDAP                           | Messaggio Win32                               | Descrizione                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **\_operazione LDAP riuscita**                      | **Nessun \_ errore**                               | Operazione riuscita.                             |
| 0x80070005L      | **\_diritti di insufficienza LDAP \_**         | **ERRORE di \_ accesso \_ negato**                   | L'utente non dispone di diritti di accesso sufficienti.             |
| 0x80070008L      | **\_Nessuna \_ memoria LDAP**                   | **ERRORE \_ di \_ memoria insufficiente \_**              | Memoria del sistema insufficiente.                         |
| 0x8007001fL      | **\_altro LDAP**                        | **ERRORE \_ gen \_ errore**                     | Errore sconosciuto.                                   |
| 0x800700eaL      | **\_risultati parziali LDAP \_**             | **ERRORE di \_ più \_ dati**                       | Sono stati ricevuti risultati parziali e riferimenti.          |
| 0x800700eaL      | **LDAP \_ altri \_ Risultati \_ da \_ restituire**    | **ERRORE di \_ più \_ dati**                       | Verranno restituiti più risultati.                 |
| 0x800704c7L      | **\_utente LDAP \_ annullato**              | **ERRORE \_ annullato**                        | L'utente ha annullato l'operazione.                     |
| 0x800704c9L      | **\_errore di connessione LDAP \_**               | **\_connessione errore \_ rifiutata**              | Impossibile stabilire la connessione.                 |
| 0x8007052eL      | **\_credenziali LDAP non valide \_**         | **ERRORE di \_ accesso non \_ riuscito**                   | Le credenziali specificate non sono valide.                |
| 0x800705b4L      | **\_timeout LDAP**                      | **\_timeout errore**                          | Timeout della ricerca.                                |
| 0x80071392L      | **LDAP \_ già \_ esistente**              | **l' \_ oggetto \_ Error \_ esiste già**          | Oggetto già esistente.                           |
| 0x8007200aL      | **\_ \_ questo attributo non \_ è LDAP**          | **ERRORE \_ DS \_ nessun \_ attributo \_ o \_ valore**     | L'attributo richiesto non esiste.              |
| 0x8007200bL      | **\_sintassi non valida LDAP \_**              | **ERRORE della \_ sintassi degli attributi di DS \_ non valida \_ \_**   | Sintassi non valida.                             |
| 0x8007200cL      | **\_tipo non definito \_ LDAP**              | **\_tipo di attributo DS per errori non \_ \_ \_ definito**   | Tipo non definito.                                |
| 0x8007200dL      | **\_attributo \_ o valore \_ LDAP \_ esistente** | **il \_ valore o l'attributo DS dell'errore \_ \_ \_ \_ esiste** | L'attributo esiste o il valore è stato assegnato. |
| 0x8007200eL      | **LDAP \_ occupato**                         | **ERRORE \_ DS \_ occupato**                         | Il server è occupato.                                  |
| 0x8007200fL      | **LDAP non \_ disponibile**                  | **ERRORE \_ DS non \_ disponibile**                  | Il server non è disponibile.                         |
| 0x80072014L      | **\_violazione della \_ classe di oggetti LDAP \_**     | **\_violazione della \_ \_ classe obj \_ di errore DS**        | Violazione della classe dell'oggetto.                          |
| 0x80072015L      | **LDAP \_ non \_ consentito \_ su non \_ foglia**    | **ERRORE \_ DS \_ \_ non in \_ \_ foglia**          | Operazione non consentita su un oggetto non foglia.  |
| 0x80072016L      | **LDAP \_ non \_ consentito \_ in \_ RDN**        | **errore \_ DS \_ \_ di errore su \_ RDN**                | Operazione non consentita su un RDN.              |
| 0x80072017L      | **LDAP \_ Nessuna \_ classe di oggetti \_ \_ mods**      | **ERRORE \_ DS \_ \_ mod cant \_ \_ classe obj**        | Impossibile modificare la classe di oggetti.                      |
| 0x80072020L      | **\_errore operazioni \_ LDAP**            | **errore \_ operazioni DS errore \_ \_**            | Si è verificato un errore dell'operazione.                        |
| 0x80072021L      | **\_errore del protocollo LDAP \_**              | **errore \_ del \_ protocollo DS di errore \_**              | Si è verificato un errore di protocollo.                         |
| 0x80072022L      | **limite di timeout LDAP \_ \_ superato**          | **superato il limite di timeout \_ DS \_ \_**          | Limite di tempo superato.                             |
| 0x80072023L      | **\_SIZELIMIT LDAP \_ superato**          | **ERRORE \_ DS \_ SIZELIMIT \_ superato**          | È stato superato il limite di dimensioni.                             |
| 0x80072024L      | **\_limite di amministrazione LDAP \_ \_ superato**       | **\_ \_ superato limite di amministrazione DS \_ per \_ errori**       | Limite di amministrazione superato nel server.     |
| 0x80072025L      | **\_confronto LDAP \_ false**               | **ERRORE \_ DS \_ confronto \_ false**               | Compare restituito **false**.                       |
| 0x80072026L      | **\_confronto LDAP \_ true**                | **ERRORE \_ DS \_ compare \_ true**                | Compare restituisce **true**.                        |
| 0x80072027L      | **\_metodo di autenticazione LDAP \_ \_ non \_ supportato** | **il \_ metodo di autenticazione DS con errori \_ non è \_ \_ \_ supportato** | Il metodo di autenticazione non è supportato.      |
| 0x80072028L      | **\_autenticazione avanzata \_ LDAP \_ obbligatoria**       | **ERRORE \_ \_ autenticazione avanzata \_ DS \_ necessaria**       | È richiesta l'autenticazione avanzata.               |
| 0x80072029L      | **autenticazione LDAP non \_ appropriata \_**          | **\_autenticazione non \_ appropriata di DS per gli errori \_**          | L'autenticazione non è appropriata.                 |
| 0x8007202aL      | **\_autenticazione LDAP \_ sconosciuta**                | **ERRORE \_ di \_ autenticazione DS non \_ noto**                | Si è verificato un errore di autenticazione sconosciuto.           |
| 0x8007202bL      | **\_riferimento LDAP**                     | **\_segnalazione errori DS \_**                     | Non è possibile risolvere il riferimento.                         |
| 0x8007202cL      | **estensione del critico LDAP non \_ disponibile \_ \_** | **ERRORE \_ DS non disponibile per l' \_ \_ estensione del critico \_** | L'estensione critica non è disponibile.               |
| 0x8007202dL      | **\_riservatezza LDAP \_ obbligatoria**    | **ERRORE \_ \_ riservato DS \_ obbligatorio**    | È necessaria la riservatezza.                     |
| 0x8007202eL      | **\_corrispondenza non appropriata \_ LDAP**      | **ERRORE \_ DS non \_ appropriato \_ corrispondente**      | Corrispondenze non appropriate.             |
| 0x8007202fL      | **\_violazione del vincolo LDAP \_**        | **\_violazione del \_ vincolo \_ DS di errore**        | Si è verificata una violazione di vincolo.                 |
| 0x80072030L      | **LDAP \_ non è un \_ oggetto di questo tipo \_**             | **ERRORE \_ DS \_ nessun \_ oggetto di questo tipo \_**             | Oggetto inesistente.                           |
| 0x80072031L      | **\_problema alias \_ LDAP**               | **\_ \_ problema alias DS \_ errore**               | Alias non valido.                              |
| 0x80072032L      | **\_sintassi DN non valida LDAP \_ \_**          | **ERRORE \_ DS \_ \_ sintassi DN non valida \_**          | La sintassi del nome distinto non è valida. |
| 0x80072033L      | **LDAP \_ è \_ foglia**                     | **l'errore \_ DS \_ è \_ foglia**                     | L'oggetto è una foglia.                            |
| 0x80072034L      | **\_problema di alias LDAP \_ Deref \_**        | **ERRORE \_ \_ Deref alias \_ DS \_**        | Non è possibile dereferenziare l'alias.                    |
| 0x80072035L      | **non è \_ possibile \_ \_ eseguire LDAP**       | **ERRORE \_ DS \_ che non verrà \_ \_ eseguito**       | Il server non è in grado di eseguire l'operazione.                 |
| 0x80072036L      | **\_rilevamento del ciclo LDAP \_**                 | **\_ \_ rilevamento ciclo DS \_ errore**                 | Il ciclo è stato rilevato.                               |
| 0x80072037L      | **\_violazione di denominazione LDAP \_**            | **\_violazione di \_ denominazione \_ DS errore**            | Si è verificata una violazione di denominazione.                    |
| 0x80072038L      | **\_risultati LDAP \_ troppo \_ grandi**          | **ERRORE \_ \_ dei risultati di un oggetto DS \_ \_ troppo \_ grande**  | Il set di risultati è troppo grande.                        |
| 0x80072039L      | **LDAP \_ interessa \_ più \_ DSA**      | **ERRORE \_ DS \_ influiscono su \_ più \_ DSA**      | Sono interessati più agenti del servizio di directory.  |
| 0x8007203aL      | **\_server LDAP \_ inattivo**                 | **ERRORE \_ nel \_ server \_ DS**                 | Impossibile contattare il server LDAP.                  |
| 0x8007203bL      | **\_errore locale \_ LDAP**                 | **errore \_ locale DS errore \_ \_**                 | Si è verificato un errore locale.                            |
| 0x8007203cL      | **\_errore di codifica LDAP \_**              | **errore \_ di \_ codifica DS errore \_**              | Si è verificato un errore di codifica.                         |
| 0x8007203dL      | **\_errore di decodifica \_ LDAP**              | **\_errore di \_ decodifica DS di errore \_**              | Si è verificato un errore di decodifica.                         |
| 0x8007203eL      | **\_errore filtro \_ LDAP**                | **ERRORE \_ \_ filtro DS \_ sconosciuto**              | Il filtro di ricerca non è valido.                        |
| 0x8007203fL      | **\_errore param \_ LDAP**                 | **errore \_ di \_ param DS errore \_**                 | Un parametro non valido è stato passato a una funzione.        |
| 0x80072040L      | **LDAP \_ non \_ supportato**               | **ERRORE \_ DS \_ non \_ supportato**               | Funzionalità non supportata.                           |
| 0x80072041L      | **\_nessun \_ risultato \_ restituito da LDAP**        | **ERRORE \_ DS \_ nessun \_ risultato \_ restituito**        | I risultati non vengono restituiti.                        |
| 0x80072042L      | **il \_ controllo LDAP non è stato \_ \_ trovato**          | **ERRORE \_ \_ controllo DS \_ non \_ trovato**          | Il controllo non è stato trovato.                           |
| 0x80072043L      | **\_ciclo client \_ LDAP**                 | **ERRORE \_ \_ ciclo client \_ DS**                 | Il ciclo client è stato rilevato.                        |
| 0x80072044L      | **\_limite di riferimento LDAP \_ \_ superato**    | **\_limite di riferimento DS per errori \_ \_ \_ superato**    | È stato superato il limite di riferimento.                         |



 

 

 





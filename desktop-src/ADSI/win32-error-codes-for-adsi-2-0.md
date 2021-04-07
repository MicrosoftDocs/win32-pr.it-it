---
title: Codici di errore Win32 per ADSI 2,0
description: Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI 2,0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 per ADSI 2,0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e079fa6a98df28625f6307f774ce194712a52a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855226"
---
# <a name="win32-error-codes-for-adsi-20"></a>Codici di errore Win32 per ADSI 2,0

Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI 2,0.



| Valore di errore ADSI | Messaggio LDAP                           | Messaggio Win32                        | Descrizione                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **\_operazione LDAP riuscita**                      | **Nessun \_ errore**                        | Operazione riuscita.                                 |
| 0x80070002       | **LDAP \_ non è un \_ oggetto di questo tipo \_**             | **FILE di errore \_ \_ non \_ trovato**          | Oggetto inesistente.                               |
| 0x80070005       | **\_metodo di autenticazione LDAP \_ \_ non \_ supportato** | **ERRORE di \_ accesso \_ negato**            | Metodo di autenticazione non supportato.                 |
| 0x80070005       | **\_autenticazione avanzata \_ LDAP \_ obbligatoria**       | **ERRORE di \_ accesso \_ negato**            | Richiede un'autenticazione avanzata.                      |
| 0x80070005       | **autenticazione LDAP non \_ appropriata \_**          | **ERRORE di \_ accesso \_ negato**            | Autenticazione non appropriata.                        |
| 0x80070005       | **\_diritti di insufficienza LDAP \_**         | **ERRORE di \_ accesso \_ negato**            | L'utente non dispone di diritti di accesso sufficienti.                 |
| 0x80070005       | **\_autenticazione LDAP \_ sconosciuta**                | **ERRORE di \_ accesso \_ negato**            | Si è verificato un errore di autenticazione sconosciuto.               |
| 0x80070008       | **\_Nessuna \_ memoria LDAP**                   | **ERRORE \_ di \_ memoria insufficiente \_**       | Memoria del sistema insufficiente.                             |
| 0x8007001F       | **\_altro LDAP**                        | **ERRORE \_ gen \_ errore**              | Si è verificato un errore sconosciuto.                              |
| 0x8007001F       | **\_errore locale \_ LDAP**                 | **ERRORE \_ gen \_ errore**              | Si è verificato un errore locale.                                |
| 0x80070037       | **LDAP non \_ disponibile**                  | **ERRORE \_ dev \_ non \_ esiste**           | Il server non è disponibile.                             |
| 0x8007003A       | **\_server LDAP \_ inattivo**                 | **ERRORE \_ \_ net \_ resp errato**            | Impossibile contattare il server LDAP.                      |
| 0x8007003B       | **\_errore di codifica LDAP \_**              | **ERRORE \_ UNEXP \_ net \_ Err**           | Si è verificato un errore di codifica.                             |
| 0x8007003B       | **\_errore di decodifica \_ LDAP**              | **ERRORE \_ UNEXP \_ net \_ Err**           | Si è verificato un errore di decodifica.                             |
| 0x80070044       | **\_limite di amministrazione LDAP \_ \_ superato**       | **ERRORE di un \_ numero eccessivo di \_ \_ nomi**          | Limite di amministrazione superato nel server.         |
| 0x80070056       | **\_credenziali LDAP non valide \_**         | **ERRORE \_ di \_ password non valida**         | Credenziale non valida.                                |
| 0x80070057       | **\_sintassi DN non valida LDAP \_ \_**          | **ERRORE \_ parametro non valido \_**        | La sintassi del nome distinto non è valida.     |
| 0x80070057       | **\_violazione di denominazione LDAP \_**            | **ERRORE \_ parametro non valido \_**        | Violazione di denominazione.                                    |
| 0x80070057       | **\_violazione della \_ classe di oggetti LDAP \_**     | **ERRORE \_ parametro non valido \_**        | Violazione della classe dell'oggetto.                              |
| 0x80070057       | **\_errore filtro \_ LDAP**                | **ERRORE \_ parametro non valido \_**        | Il filtro di ricerca non è valido.                                |
| 0x80070057       | **\_errore param \_ LDAP**                 | **ERRORE \_ parametro non valido \_**        | Parametro non valido passato a una routine.               |
| 0X8007006E       | **\_errore operazioni \_ LDAP**            | **ERRORE di \_ apertura \_ non riuscito**              | Si è verificato un errore dell'operazione.                            |
| 0x8007007A       | **\_risultati LDAP \_ troppo \_ grandi**          | **ERRORE \_ buffer insufficiente \_**      | Il set di risultati è troppo grande.                            |
| 0x8007007B       | **\_sintassi non valida LDAP \_**              | **ERRORE \_ nome non valido \_**             | Sintassi non valida.                                    |
| 0x8007007C       | **\_errore del protocollo LDAP \_**              | **ERRORE \_ livello non valido \_**            | Errore del protocollo.                                      |
| 0x800700B7       | **LDAP \_ già \_ esistente**              | **ERRORE \_ già \_ esistente**           | Oggetto già esistente.                               |
| 0x800700EA       | **\_risultati parziali LDAP \_**             | **ERRORE di \_ più \_ dati**                | Sono stati ricevuti risultati parziali e riferimenti.              |
| 0x800700EA       | **LDAP \_ occupato**                         | **ERRORE \_ occupato**                      | Il server è occupato.                                      |
| 0x800703EB       | **non è \_ possibile \_ \_ eseguire LDAP**       | **\_non è \_ possibile \_ completare l'errore**        | Il server non è in grado di eseguire l'operazione.                     |
| 0x8007041D       | **\_timeout LDAP**                      | **\_timeout della \_ richiesta del servizio di errore \_** | Timeout della ricerca.                                    |
| 0x800704B8       | **\_confronto LDAP \_ false**               | **errore \_ esteso \_ errore**           | Compare restituito **false**.                           |
| 0x800704B8       | **\_confronto LDAP \_ true**                | **errore \_ esteso \_ errore**           | Compare restituisce **true**.                            |
| 0x800704B8       | **\_riferimento LDAP**                     | **errore \_ esteso \_ errore**           | Non è possibile risolvere il riferimento.                             |
| 0x800704B8       | **estensione del critico LDAP non \_ disponibile \_ \_** | **errore \_ esteso \_ errore**           | L'estensione critica non è disponibile.                   |
| 0x800704B8       | **\_ \_ questo attributo non \_ è LDAP**          | **errore \_ esteso \_ errore**           | L'attributo richiesto non esiste.                  |
| 0x800704B8       | **\_tipo non definito \_ LDAP**              | **errore \_ esteso \_ errore**           | Il tipo non è definito.                                 |
| 0x800704B8       | **\_corrispondenza non appropriata \_ LDAP**      | **errore \_ esteso \_ errore**           | Corrispondenze non appropriate.                 |
| 0x800704B8       | **\_violazione del vincolo LDAP \_**        | **errore \_ esteso \_ errore**           | Si è verificata una violazione di vincolo.                     |
| 0x800704B8       | **\_attributo \_ o valore \_ LDAP \_ esistente** | **errore \_ esteso \_ errore**           | L'attributo esiste o il valore è stato assegnato. |
| 0x800704B8       | **\_problema alias \_ LDAP**               | **errore \_ esteso \_ errore**           | Alias non valido.                                  |
| 0x800704B8       | **LDAP \_ è \_ foglia**                     | **errore \_ esteso \_ errore**           | L'oggetto è una foglia.                                    |
| 0x800704B8       | **\_problema di alias LDAP \_ Deref \_**        | **errore \_ esteso \_ errore**           | Non è possibile dereferenziare l'alias.                        |
| 0x800704B8       | **\_rilevamento del ciclo LDAP \_**                 | **errore \_ esteso \_ errore**           | Il ciclo è stato rilevato.                                   |
| 0x800704B8       | **LDAP \_ non \_ consentito \_ su non \_ foglia**    | **errore \_ esteso \_ errore**           | Operazione non consentita su un oggetto non foglia.       |
| 0x800704B8       | **LDAP \_ non \_ consentito \_ in \_ RDN**        | **errore \_ esteso \_ errore**           | Operazione non consentita su RDN.                     |
| 0x800704B8       | **LDAP \_ Nessuna \_ classe di oggetti \_ \_ mods**      | **errore \_ esteso \_ errore**           | Impossibile modificare la classe di oggetti.                          |
| 0x800704B8       | **LDAP \_ interessa \_ più \_ DSA**      | **errore \_ esteso \_ errore**           | Sono interessati più agenti del servizio di directory.      |
| 0x800704C7       | **\_utente LDAP \_ annullato**              | **ERRORE \_ annullato**                 | L'operazione è stata annullata dall'utente.                     |
| 0x80070718       | **limite di timeout LDAP \_ \_ superato**          | **ERRORE \_ di \_ quota insufficiente \_**        | Limite di tempo superato.                                 |
| 0x80070718       | **\_SIZELIMIT LDAP \_ superato**          | **ERRORE \_ di \_ quota insufficiente \_**        | È stato superato il limite di dimensioni.                                 |



 

In ADSI 2,0, diversi messaggi di errore LDAP vengono mappati a un codice di errore Win32 come errore **\_ esteso \_ errore**. Chiamare [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) per recuperare la stringa di errore restituita dal server. Per ulteriori informazioni, vedere [i messaggi di errore estesi di ADSI](adsi-extended-error-messages.md) .

 

 





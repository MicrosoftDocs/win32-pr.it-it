---
title: Codici di errore Win32
description: Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d1986b0de2e4afeed0fccdcce62851acfaf104c3f360b7ea462410f4484f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118689891"
---
# <a name="win32-error-codes"></a>Codici di errore Win32

Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI.



| Valore di errore ADSI | Messaggio LDAP                           | Messaggio Win32                               | Descrizione                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **LDAP \_ RIUSCITO**                      | **NESSUN \_ ERRORE**                               | Operazione riuscita.                             |
| 0x80070005L      | **DIRITTI \_ LDAP \_ INSUFFICIENTI**         | **ERRORE \_ DI ACCESSO \_ NEGATO**                   | L'utente non dispone di diritti di accesso sufficienti.             |
| 0x80070008L      | **LDAP \_ NO \_ MEMORY**                   | **MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**              | Memoria insufficiente per il sistema.                         |
| 0x8007001fL      | **LDAP \_ OTHER**                        | **ERRORE \_ GEN \_ ERRORE**                     | Errore sconosciuto.                                   |
| 0x800700eaL      | **RISULTATI \_ PARZIALI \_ LDAP**             | **ERRORE \_ - ALTRI \_ DATI**                       | Risultati parziali e segnalazioni ricevuti.          |
| 0x800700eaL      | **LDAP \_ ALTRI RISULTATI DA \_ \_ \_ RESTITUIRE**    | **ERRORE \_ - ALTRI \_ DATI**                       | Devono essere restituiti altri risultati.                 |
| 0x800704c7L      | **UTENTE LDAP \_ \_ ANNULLATO**              | **ERRORE \_ ANNULLATO**                        | L'utente ha annullato l'operazione.                     |
| 0x800704c9L      | **ERRORE \_ DI CONNESSIONE \_ LDAP**               | **CONNESSIONE \_ ERRORE \_ RIFIUTATA**              | Impossibile stabilire la connessione.                 |
| 0x8007052eL      | **CREDENZIALI \_ LDAP NON \_ VALIDE**         | **ERRORE \_ DURANTE \_ L'ACCESSO**                   | La credenziale fornita non è valida.                |
| 0x800705b4L      | **LDAP \_ TIMEOUT**                      | **\_TIMEOUT ERRORE**                          | Timeout della ricerca.                                |
| 0x80071392L      | **LDAP \_ ESISTE \_ GIÀ**              | **\_L'OGGETTO \_ ERRORE ESISTE \_ GIÀ**          | Oggetto già esistente.                           |
| 0x8007200aL      | **LDAP \_ NESSUN ATTRIBUTO DI QUESTO \_ \_ TIPO**          | **ERRORE \_ DS \_ NESSUN ATTRIBUTO O \_ \_ \_ VALORE**     | L'attributo richiesto non esiste.              |
| 0x8007200bL      | **SINTASSI \_ LDAP NON \_ VALIDA**              | **ERRORE \_ SINTASSI \_ DELL'ATTRIBUTO DS NON \_ \_ VALIDA**   | Sintassi non valida.                             |
| 0x8007200cL      | **TIPO \_ LDAP NON \_ DEFINITO**              | **ERRORE \_ TIPO DI ATTRIBUTO DS NON \_ \_ \_ DEFINITO**   | Tipo non definito.                                |
| 0x8007200dL      | **ATTRIBUTO O VALORE LDAP \_ \_ \_ \_ ESISTENTE** | **ERRORE \_ DELL'ATTRIBUTO \_ O DEL VALORE \_ \_ DS \_ ESISTENTE** | L'attributo esiste o il valore è stato assegnato. |
| 0x8007200eL      | **LDAP \_ OCCUPATO**                         | **ERRORE \_ DS \_ OCCUPATO**                         | Il server è occupato.                                  |
| 0x8007200fL      | **LDAP \_ NON DISPONIBILE**                  | **ERRORE \_ DS \_ NON DISPONIBILE**                  | Il server non è disponibile.                         |
| 0x80072014L      | **VIOLAZIONE \_ DELLA CLASSE DI OGGETTI \_ \_ LDAP**     | **ERRORE \_ DI VIOLAZIONE \_ DELLA CLASSE OBJ \_ DS \_**        | Violazione della classe di oggetti.                          |
| 0x80072015L      | **LDAP \_ NON CONSENTITO IN \_ \_ \_ NONLEAF**    | **ERRORE \_ DS \_ CANT \_ ON NON \_ \_ LEAF**          | L'operazione non è consentita su un oggetto non foglia.  |
| 0x80072016L      | **LDAP \_ NON CONSENTITO IN \_ \_ \_ RDN**        | **ERRORE \_ DS \_ CANT \_ IN \_ RDN**                | L'operazione non è consentita in un RDN.              |
| 0x80072017L      | **LDAP \_ NO \_ OBJECT \_ CLASS \_ MODS**      | **CLASSE \_ OBJ ERROR DS \_ CANT \_ \_ \_ MOD**        | Impossibile modificare la classe dell'oggetto.                      |
| 0x80072020L      | **ERRORE \_ DELLE OPERAZIONI \_ LDAP**            | **ERRORE \_ DELLE OPERAZIONI DS \_ \_**            | Si è verificato un errore di operazione.                        |
| 0x80072021L      | **ERRORE \_ DEL PROTOCOLLO \_ LDAP**              | **ERRORE \_ DEL PROTOCOLLO DS \_ \_**              | Si è verificato un errore di protocollo.                         |
| 0x80072022L      | **LIMITE DI TEMPO LDAP \_ \_ SUPERATO**          | **ERRORE \_ DS \_ TIMELIMIT \_ SUPERATO**          | Limite di tempo superato.                             |
| 0x80072023L      | **LDAP \_ SIZELIMIT \_ EXCEEDED**          | **ERRORE \_ DS \_ SIZELIMIT \_ SUPERATO**          | È stato superato il limite di dimensioni.                             |
| 0x80072024L      | **LIMITE \_ DI AMMINISTRAZIONE LDAP \_ \_ SUPERATO**       | **ERRORE \_ DS \_ ADMIN LIMIT \_ \_ EXCEEDED**       | È stato superato il limite di amministrazione nel server.     |
| 0x80072025L      | **LDAP \_ COMPARE \_ FALSE**               | **ERRORE \_ DS \_ COMPARE \_ FALSE**               | Il confronto ha **restituito FALSE.**                       |
| 0x80072026L      | **LDAP \_ COMPARE \_ TRUE**                | **ERRORE \_ DS \_ COMPARE \_ TRUE**                | Il confronto ha prodotto **TRUE.**                        |
| 0x80072027L      | **METODO DI AUTENTICAZIONE LDAP \_ \_ NON \_ \_ SUPPORTATO** | **ERRORE \_ METODO DI AUTENTICAZIONE \_ DS NON \_ \_ \_ SUPPORTATO** | Il metodo di autenticazione non è supportato.      |
| 0x80072028L      | **LDAP \_ STRONG \_ AUTH \_ REQUIRED**       | **ERRORE \_ DS \_ STRONG \_ AUTH \_ REQUIRED**       | È necessaria l'autenticazione avanzata.               |
| 0x80072029L      | **AUTENTICAZIONE LDAP \_ \_ INAPPROPRIATA**          | **ERRORE \_ DS \_ INAPPROPRIATE \_ AUTH**          | L'autenticazione non è appropriata.                 |
| 0x8007202aL      | **LDAP \_ AUTH \_ UNKNOWN**                | **ERRORE \_ DS \_ AUTH \_ UNKNOWN**                | Si è verificato un errore di autenticazione sconosciuto.           |
| 0x8007202bL      | **SEGNALAZIONE \_ LDAP**                     | **SEGNALAZIONE \_ ERRORE DS \_**                     | Non è possibile risolvere la segnalazione.                         |
| 0x8007202cL      | **ESTENSIONE DEL \_ CRITERIO LDAP NON \_ \_ DISPONIBILE** | **ERRORE \_ DS \_ UNAVAILABLE \_ CRIT \_ EXTENSION** | L'estensione critica non è disponibile.               |
| 0x8007202dL      | **RISERVATEZZA LDAP \_ \_ OBBLIGATORIA**    | **ERRORE \_ DS \_ CONFIDENTIALITY \_ REQUIRED**    | La riservatezza è obbligatoria.                     |
| 0x8007202eL      | **CORRISPONDENZA LDAP \_ INAPPROPRIATA \_**      | **ERRORE DI \_ CORRISPONDENZA \_ INAPPROPRIATA DS \_**      | Si è verificata una corrispondenza inappropriata.             |
| 0x8007202fL      | **VIOLAZIONE \_ DEL \_ VINCOLO LDAP**        | **ERRORE DI \_ VIOLAZIONE DEL VINCOLO DS \_ \_**        | Si è verificata una violazione del vincolo.                 |
| 0x80072030L      | **LDAP \_ NO \_ SUCH \_ OBJECT**             | **ERRORE \_ DS \_ NO SUCH \_ \_ OBJECT**             | L'oggetto non esiste.                           |
| 0x80072031L      | **PROBLEMA \_ CON L'ALIAS \_ LDAP**               | **ERRORE DEL \_ PROBLEMA RELATIVO \_ ALL'ALIAS DS \_**               | Alias non valido.                              |
| 0x80072032L      | **SINTASSI \_ \_ DN LDAP NON \_ VALIDA**          | **SINTASSI \_ DN \_ \_ DS NON \_ VALIDA**          | La sintassi del nome distinto non è valida. |
| 0x80072033L      | **LDAP \_ IS \_ LEAF**                     | **ERRORE \_ DS \_ IS \_ LEAF**                     | L'oggetto è una foglia.                            |
| 0x80072034L      | **PROBLEMA \_ DI \_ DEREF DELL'ALIAS \_ LDAP**        | **ERRORE \_ DEL PROBLEMA DI \_ \_ DEREF DELL'ALIAS DS \_**        | Impossibile dereferenziare l'alias.                    |
| 0x80072035L      | **LDAP \_ CHE NON È IN GRADO DI \_ \_ ESEGUIRE**       | **ERRORE \_ CHE DS \_ NON È IN GRADO DI \_ \_ ESEGUIRE**       | Il server non può eseguire l'operazione.                 |
| 0x80072036L      | **RILEVAMENTO \_ CICLO \_ LDAP**                 | **ERRORE \_ DI RILEVAMENTO DEL CICLO DS \_ \_**                 | È stato rilevato un ciclo.                               |
| 0x80072037L      | **VIOLAZIONE \_ DI \_ DENOMINAZIONE LDAP**            | **ERRORE DI \_ VIOLAZIONE DI \_ DENOMINAZIONE DS \_**            | Si è verificata una violazione di denominazione.                    |
| 0x80072038L      | **RISULTATI \_ LDAP \_ TROPPO \_ GRANDI**          | **ERRORE \_ NEI RISULTATI \_ DELL'OGGETTO \_ DS TROPPO \_ \_ GRANDI**  | Il set di risultati è troppo grande.                        |
| 0x80072039L      | **LDAP \_ \_ INFLUISCE \_ SU PIÙ DSAS**      | **ERRORE \_ DS \_ INFLUISCE \_ SU PIÙ \_ DSAS**      | Sono interessati più agenti del servizio di directory.  |
| 0x8007203aL      | **LDAP \_ SERVER \_ DOWN**                 | **ERRORE \_ DS \_ SERVER \_ DOWN**                 | Impossibile contattare il server LDAP.                  |
| 0x8007203bL      | **ERRORE \_ LOCALE \_ LDAP**                 | **ERRORE \_ DS \_ LOCAL \_ ERROR**                 | Si è verificato un errore locale.                            |
| 0x8007203cL      | **ERRORE \_ DI CODIFICA \_ LDAP**              | **ERRORE \_ DI CODIFICA DS \_ \_**              | Si è verificato un errore di codifica.                         |
| 0x8007203dL      | **ERRORE \_ DI DECODIFICA \_ LDAP**              | **ERRORE \_ DI DECODIFICA DS \_ \_**              | Si è verificato un errore di decodifica.                         |
| 0x8007203eL      | **ERRORE \_ DEL FILTRO \_ LDAP**                | **ERRORE \_ DS \_ FILTER \_ UNKNOWN**              | Il filtro di ricerca non è stato applicato.                        |
| 0x8007203fL      | **ERRORE \_ DEL PARAMETRO \_ LDAP**                 | **ERRORE \_ DS \_ PARAM \_ ERROR**                 | È stato passato un parametro non valido a una funzione.        |
| 0x80072040L      | **LDAP \_ NON \_ SUPPORTATO**               | **ERRORE \_ DS \_ NON \_ SUPPORTATO**               | Funzionalità non supportata.                           |
| 0x80072041L      | **LDAP \_ NON \_ HA \_ RESTITUITO RISULTATI**        | **ERRORE \_ DS \_ NESSUN RISULTATO \_ \_ RESTITUITO**        | I risultati non vengono restituiti.                        |
| 0x80072042L      | **CONTROLLO \_ LDAP \_ NON \_ TROVATO**          | **ERRORE \_ DEL CONTROLLO DS NON \_ \_ \_ TROVATO**          | Controllo non trovato.                           |
| 0x80072043L      | **CICLO \_ CLIENT \_ LDAP**                 | **CICLO \_ CLIENT DS \_ \_ ERRORE**                 | È stato rilevato un ciclo client.                        |
| 0x80072044L      | **LIMITE \_ DI \_ \_ SEGNALAZIONI LDAP SUPERATO**    | **LIMITE \_ SEGNALAZIONE DS \_ DI ERRORE \_ \_ SUPERATO**    | Superato il limite di segnalazioni.                         |



 

 

 





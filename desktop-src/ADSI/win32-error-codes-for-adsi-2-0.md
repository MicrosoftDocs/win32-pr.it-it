---
title: Codici di errore Win32 per ADSI 2.0
description: Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI 2.0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Codici di errore Win32 per ADSI 2.0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea81b4d277ad43cb2278d23549e370df1d11b3058be1e9c8b0f8b9329eabe26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589751"
---
# <a name="win32-error-codes-for-adsi-20"></a>Codici di errore Win32 per ADSI 2.0

Nella tabella seguente sono elencati i messaggi di errore LDAP per ADSI 2.0.



| Valore di errore ADSI | Messaggio LDAP                           | Messaggio Win32                        | Descrizione                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP \_ RIUSCITO**                      | **NESSUN \_ ERRORE**                        | Operazione riuscita.                                 |
| 0x80070002       | **LDAP \_ NESSUN OGGETTO DI QUESTO \_ \_ TIPO**             | **FILE \_ DI ERRORE NON \_ \_ TROVATO**          | L'oggetto non esiste.                               |
| 0x80070005       | **METODO \_ DI AUTENTICAZIONE LDAP NON \_ \_ \_ SUPPORTATO** | **ERRORE \_ DI ACCESSO \_ NEGATO**            | Metodo di autenticazione non supportato.                 |
| 0x80070005       | **LDAP \_ STRONG \_ AUTH \_ REQUIRED**       | **ERRORE \_ DI ACCESSO \_ NEGATO**            | Richiede l'autenticazione avanzata.                      |
| 0x80070005       | **AUTENTICAZIONE \_ LDAP \_ INAPPROPRIATA**          | **ERRORE \_ DI ACCESSO \_ NEGATO**            | Autenticazione non appropriata.                        |
| 0x80070005       | **DIRITTI \_ LDAP \_ INSUFFICIENTI**         | **ERRORE \_ DI ACCESSO \_ NEGATO**            | L'utente non dispone di diritti di accesso sufficienti.                 |
| 0x80070005       | **AUTENTICAZIONE LDAP \_ \_ SCONOSCIUTA**                | **ERRORE \_ DI ACCESSO \_ NEGATO**            | Si è verificato un errore di autenticazione sconosciuto.               |
| 0x80070008       | **LDAP \_ NO \_ MEMORY**                   | **MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**       | Memoria insufficiente per il sistema.                             |
| 0x8007001F       | **LDAP \_ OTHER**                        | **ERRORE \_ GEN \_ ERRORE**              | Si è verificato un errore sconosciuto.                              |
| 0x8007001F       | **ERRORE \_ LOCALE \_ LDAP**                 | **ERRORE \_ GEN \_ ERRORE**              | Si è verificato un errore locale.                                |
| 0x80070037       | **LDAP \_ NON DISPONIBILE**                  | **ERRORE \_ DEV \_ \_ INESISTENTE**           | Il server non è disponibile.                             |
| 0x8007003A       | **SERVER LDAP \_ \_ IN BASSO**                 | **ERRORE \_ DI RETE \_ \_ RESP NON ERTA**            | Impossibile contattare il server LDAP.                      |
| 0x8007003B       | **ERRORE \_ DI CODIFICA \_ LDAP**              | **ERRORE \_ UNEXP \_ NET \_ ERR**           | Si è verificato un errore di codifica.                             |
| 0x8007003B       | **ERRORE \_ DI DECODIFICA \_ LDAP**              | **ERRORE \_ UNEXP \_ NET \_ ERR**           | Si è verificato un errore di decodifica.                             |
| 0x80070044       | **LIMITE \_ DI AMMINISTRAZIONE LDAP \_ \_ SUPERATO**       | **ERRORE \_ TROPPI \_ \_ NOMI**          | Superato il limite di amministrazione nel server.         |
| 0x80070056       | **CREDENZIALI \_ LDAP NON \_ VALIDE**         | **ERRORE \_ PASSWORD NON \_ VALIDA**         | Credenziale non valida.                                |
| 0x80070057       | **SINTASSI \_ \_ DN LDAP NON \_ VALIDA**          | **ERRORE \_ PARAMETRO NON \_ VALIDO**        | La sintassi del nome distinto non è valida.     |
| 0x80070057       | **VIOLAZIONE \_ DI \_ DENOMINAZIONE LDAP**            | **ERRORE \_ PARAMETRO NON \_ VALIDO**        | Violazione di denominazione.                                    |
| 0x80070057       | **VIOLAZIONE \_ DELLA CLASSE DI OGGETTI \_ \_ LDAP**     | **ERRORE \_ PARAMETRO NON \_ VALIDO**        | Violazione della classe di oggetti.                              |
| 0x80070057       | **ERRORE \_ DEL FILTRO \_ LDAP**                | **ERRORE \_ PARAMETRO NON \_ VALIDO**        | Il filtro di ricerca non è stato applicato.                                |
| 0x80070057       | **ERRORE \_ DEL PARAMETRO \_ LDAP**                 | **ERRORE \_ PARAMETRO NON \_ VALIDO**        | Il parametro non valido è stato passato a una routine.               |
| 0X8007006E       | **ERRORE \_ DELLE OPERAZIONI \_ LDAP**            | **ERRORE \_ DI APERTURA NON \_ RIUSCITA**              | Si è verificato un errore di operazione.                            |
| 0x8007007A       | **RISULTATI \_ LDAP \_ TROPPO \_ GRANDI**          | **ERRORE \_ BUFFER \_ INSUFFICIENTE**      | Il set di risultati è troppo grande.                            |
| 0x8007007B       | **SINTASSI \_ LDAP NON \_ VALIDA**              | **ERRORE \_ NOME NON \_ VALIDO**             | Sintassi non valida.                                    |
| 0x8007007C       | **ERRORE \_ DEL PROTOCOLLO \_ LDAP**              | **LIVELLO \_ DI ERRORE NON \_ VALIDO**            | Errore di protocollo.                                      |
| 0x800700B7       | **LDAP \_ ESISTE \_ GIÀ**              | **ERRORE \_ GIÀ \_ ESISTENTE**           | Oggetto già esistente.                               |
| 0x800700EA       | **RISULTATI \_ PARZIALI \_ LDAP**             | **ERROR \_ MORE \_ DATA**                | Risultati parziali e segnalazioni ricevute.              |
| 0x800700EA       | **LDAP \_ OCCUPATO**                         | **ERRORE \_ OCCUPATO**                      | Il server è occupato.                                      |
| 0x800703EB       | **LDAP \_ CHE NON È IN GRADO DI \_ \_ ESEGUIRE**       | **IMPOSSIBILE \_ \_ COMPLETARE \_ L'ERRORE**        | Il server non può eseguire l'operazione.                     |
| 0x8007041D       | **LDAP \_ TIMEOUT**                      | **ERROR \_ SERVICE REQUEST TIMEOUT (TIMEOUT RICHIESTA SERVIZIO \_ \_ ERRORI)** | Timeout della ricerca.                                    |
| 0x800704B8       | **LDAP \_ COMPARE \_ FALSE**               | **ERRORE \_ ESTESO \_ ERRORE**           | Il confronto ha **restituito FALSE.**                           |
| 0x800704B8       | **LDAP \_ COMPARE \_ TRUE**                | **ERRORE \_ ESTESO \_ ERRORE**           | Il confronto ha prodotto **TRUE.**                            |
| 0x800704B8       | **SEGNALAZIONE \_ LDAP**                     | **ERRORE \_ ESTESO \_ ERRORE**           | Non è possibile risolvere la segnalazione.                             |
| 0x800704B8       | **ESTENSIONE DEL \_ CRITERIO LDAP NON \_ \_ DISPONIBILE** | **ERRORE \_ ESTESO \_ ERRORE**           | L'estensione critica non è disponibile.                   |
| 0x800704B8       | **LDAP \_ NO \_ SUCH \_ ATTRIBUTE**          | **ERRORE \_ ESTESO \_ ERRORE**           | L'attributo richiesto non esiste.                  |
| 0x800704B8       | **TIPO \_ LDAP NON \_ DEFINITO**              | **ERRORE \_ ESTESO \_ ERRORE**           | Il tipo non è definito.                                 |
| 0x800704B8       | **CORRISPONDENZA LDAP \_ INAPPROPRIATA \_**      | **ERRORE \_ ESTESO \_ ERRORE**           | Si è verificata una corrispondenza inappropriata.                 |
| 0x800704B8       | **VIOLAZIONE \_ DEL \_ VINCOLO LDAP**        | **ERRORE \_ ESTESO \_ ERRORE**           | Si è verificata una violazione del vincolo.                     |
| 0x800704B8       | **ATTRIBUTO O VALORE LDAP \_ \_ \_ \_ ESISTENTE** | **ERRORE \_ ESTESO \_ ERRORE**           | L'attributo esiste o il valore è stato assegnato. |
| 0x800704B8       | **PROBLEMA \_ CON L'ALIAS \_ LDAP**               | **ERRORE \_ ESTESO \_ ERRORE**           | Alias non valido.                                  |
| 0x800704B8       | **LDAP \_ IS \_ LEAF**                     | **ERRORE \_ ESTESO \_ ERRORE**           | L'oggetto è una foglia.                                    |
| 0x800704B8       | **PROBLEMA \_ DI \_ DEREF DELL'ALIAS \_ LDAP**        | **ERRORE \_ ESTESO \_ ERRORE**           | Impossibile dereferenziare l'alias.                        |
| 0x800704B8       | **RILEVAMENTO \_ CICLO \_ LDAP**                 | **ERRORE \_ ESTESO \_ ERRORE**           | È stato rilevato un ciclo.                                   |
| 0x800704B8       | **LDAP \_ NON CONSENTITO IN \_ \_ \_ NONAF**    | **ERRORE \_ ESTESO \_ ERRORE**           | Operazione non consentita su un oggetto non foglia.       |
| 0x800704B8       | **LDAP \_ NON CONSENTITO SU \_ \_ \_ RDN**        | **ERRORE \_ ESTESO \_ ERRORE**           | L'operazione non è consentita in RDN.                     |
| 0x800704B8       | **LDAP \_ NO \_ OBJECT \_ CLASS \_ MODS**      | **ERRORE \_ ESTESO \_ ERRORE**           | Impossibile modificare la classe di oggetti.                          |
| 0x800704B8       | **LDAP \_ \_ INFLUISCE \_ SU PIÙ DSAS**      | **ERRORE \_ ESTESO \_ ERRORE**           | Sono interessati più agenti del servizio di directory.      |
| 0x800704C7       | **UTENTE LDAP \_ \_ ANNULLATO**              | **ERRORE \_ ANNULLATO**                 | L'utente ha annullato l'operazione.                     |
| 0x80070718       | **LIMITE DI TEMPO LDAP \_ \_ SUPERATO**          | **ERRORE \_ - \_ QUOTA INSUFFICIENTE \_**        | Limite di tempo superato.                                 |
| 0x80070718       | **LDAP \_ SIZELIMIT \_ EXCEEDED**          | **ERRORE \_ - \_ QUOTA INSUFFICIENTE \_**        | È stato superato il limite di dimensioni.                                 |



 

In ADSI 2.0 diversi messaggi di errore LDAP vengono mappati a un codice di errore Win32 come **ERRORE \_ \_ ESTESO**. Chiamare [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) per recuperare la stringa di errore restituita dal server. Per altre informazioni, vedere Messaggi [di errore estesi ADSI più](adsi-extended-error-messages.md) avanti.

 

 





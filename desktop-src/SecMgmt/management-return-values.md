---
description: Elenca i valori restituiti dalle funzioni di gestione della sicurezza.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valori restituiti dalla gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf20090ed4bbdfbeebb8fd77eafa8b9430df5aa816463ee32adb25116c7c3bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894254"
---
# <a name="security-management-return-values"></a>Valori restituiti dalla gestione della sicurezza

I valori restituiti dalla gestione della sicurezza includono quanto segue:

-   [Valori restituiti degli allegati](#attachment-return-values)
-   [Valori restituiti dalla funzione di criteri LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valori restituiti degli allegati

Il set di strumenti di configurazione della sicurezza supporta i codici **restituiti SCESTATUS** seguenti. Questi valori vengono restituiti dalle funzioni di supporto degli allegati e dalle funzioni implementate durante la scrittura di un motore di allegato o di uno snap-in.



| Valore                            | Descrizione                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ SUCCESS               | Funzione completata.                                                                          |
| PARAMETRO SCESTATUS \_ NON \_ VALIDO    | Uno dei parametri passati alla funzione non è valido.                                      |
| RECORD SCESTATUS \_ \_ NON \_ TROVATO    | Il record specificato non è stato trovato nel database di sicurezza.                                     |
| DATI SCESTATUS \_ NON \_ VALIDI         | La funzione non è riuscita perché alcuni dati non erano validi.                                             |
| OGGETTO SCESTATUS \_ \_ ESISTENTE        | L'oggetto esiste già.                                                                       |
| BUFFER SCESTATUS \_ \_ TROPPO \_ PICCOLO    | Il buffer passato alla funzione per ricevere i dati non è sufficientemente grande da ricevere tutti i dati. |
| PROFILO SCESTATUS \_ \_ NON \_ TROVATO   | Il profilo specificato non è stato trovato.                                                             |
| FORMATO SCESTATUS \_ NON \_ VALIDO           | Il formato non è valido.                                                                         |
| RISORSA SCESTATUS \_ \_ INSUFFICIENTE \_ | Memoria insufficiente.                                                                    |
| ACCESSO SCESTATUS \_ \_ NEGATO        | Il chiamante non dispone di privilegi sufficienti per completare questa azione.                          |
| SCESTATUS \_ CANT \_ DELETE          | La funzione non può eliminare l'elemento specificato.                                                   |
| OVERFLOW DEL PREFISSO \_ SCESTATUS \_      | Si è verificato un overflow del prefisso.                                                                      |
| SCESTATUS \_ OTHER \_ ERROR          | Si è verificato un errore non specificato.                                                               |
| SCESTATUS \_ GIÀ \_ IN ESECUZIONE      | Il servizio è già in esecuzione.                                                                  |
| SERVIZIO SCESTATUS \_ \_ NON \_ SUPPORTO | Il servizio specificato non è supportato.                                                          |
| SCESTATUS \_ MOD \_ NOT \_ FOUND       | Non è possibile trovare o caricare una DLL del motore degli allegati elencata nel Registro di sistema.      |
| ECCEZIONE SCESTATUS \_ \_ NEL \_ SERVER | Si è verificata un'eccezione nel server.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valori restituiti dalla funzione di criteri LSA

La [*maggior parte delle funzioni di*](/windows/desktop/SecGloss/l-gly) criteri dell'autorità di sicurezza locale (LSA) restituisce un valore NTSTATUS per indicare l'esito positivo o negativo. I vari valori NTSTATUS sono definiti in Ntstatus.h, distribuito con Microsoft Windows Driver Development Kit (DDK).

Per convertire un valore restituito NTSTATUS in un Windows errore, usare la [**funzione LsaNtStatusToWinError.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)

Nella tabella seguente sono elencati i valori NTSTATUS che possono essere restituiti da qualsiasi funzione LSA. Le sezioni del valore restituito per alcune delle funzioni LSA elencano codici di errore aggiuntivi che la funzione potrebbe restituire. In questa tabella sono elencati Windows codice di errore che corrisponde a ogni valore NTSTATUS.



| Codice NTSTATUS (Windows di errore)                                        | Significato                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| STATO \_ RIUSCITO (ERRORE \_ RIUSCITO)<br/>                               | La funzione ha avuto esito positivo.                                                                                                            |
| ACCESSO \_ ALLO STATO NEGATO \_ (ERRORE DI ACCESSO \_ \_ NEGATO)<br/>                 | Il chiamante non dispone dell'accesso appropriato per completare l'operazione.                                                                  |
| STATO \_ RISORSE \_ INSUFFICIENTI (ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA)<br/> | Le risorse di sistema, ad esempio la memoria per allocare buffer, non sono sufficienti per completare la chiamata.                                        |
| STATO \_ ERRORE INTERNO DEL DATABASE \_ \_ (ERRORE INTERNO DEL \_ \_ \_ DATABASE)<br/>       | Il database LSA contiene un'incoerenza interna.                                                                                    |
| HANDLE \_ DI STATO NON VALIDO \_ \_ (HANDLE DI ERRORE NON \_ VALIDO)<br/>               | Indica che un oggetto o un handle RPC non è valido nel [*contesto*](/windows/desktop/SecGloss/c-gly) utilizzato.     |
| STATO \_ SERVER NON VALIDO \_ \_ (ERRORE STATO SERVER NON \_ \_ \_ VALIDO)<br/> | Indica che il server LSA è attualmente disabilitato.                                                                                         |
| PARAMETRO \_ STATUS NON VALIDO \_ (ERRORE PARAMETRO NON \_ \_ VALIDO)<br/>         | Uno dei parametri non è valido.                                                                                                     |
| STATUS \_ NO \_ SUCH \_ PRIVILEGE (ERROR \_ NO \_ SUCH \_ PRIVILEGE)<br/>       | Indica che un privilegio specificato non esiste.                                                                                         |
| NOME \_ OGGETTO STATO NON TROVATO \_ \_ \_ \_ (FILE DEGLI ERRORI NON \_ \_ TROVATO)<br/>     | Impossibile trovare un oggetto nel database dei criteri LSA. L'oggetto può essere stato specificato dal SID o dal nome, a seconda del tipo. |
| STATO \_ NON RIUSCITO (ERRORE DI GENERAZIONE \_ \_ ERRORE)<br/>                     | Errore generico, ad esempio un errore di connessione RPC.                                                                                        |



 

 


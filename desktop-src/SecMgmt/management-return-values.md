---
description: Elenca i valori restituiti dalle funzioni di gestione della sicurezza.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valori restituiti per la gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316640"
---
# <a name="security-management-return-values"></a>Valori restituiti per la gestione della sicurezza

I valori restituiti per la gestione della sicurezza includono quanto segue:

-   [Valori restituiti allegati](#attachment-return-values)
-   [Valori restituiti della funzione di criteri LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valori restituiti allegati

Il set di strumenti di configurazione della sicurezza supporta i codici restituiti **SCESTATUS** seguenti. Questi valori vengono restituiti dalle funzioni di supporto degli allegati e dalle funzioni implementate durante la scrittura di un motore di allegati o di uno snap-in.



| Valore                            | Descrizione                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ riuscito               | Funzione completata.                                                                          |
| \_parametro SCESTATUS non valido \_    | Uno dei parametri passati alla funzione non è valido.                                      |
| \_record SCESTATUS \_ non \_ trovato    | Il record specificato non è stato trovato nel database di sicurezza.                                     |
| SCESTATUS \_ dati non validi \_         | La funzione non è riuscita perché alcuni dati non sono validi.                                             |
| \_oggetto SCESTATUS \_ esistente        | L'oggetto esiste già.                                                                       |
| \_buffer SCESTATUS \_ troppo \_ piccolo    | Il buffer passato nella funzione per la ricezione dei dati non è sufficientemente grande da ricevere tutti i dati. |
| \_profilo SCESTATUS \_ non \_ trovato   | Il profilo specificato non è stato trovato.                                                             |
| formato SCESTATUS non \_ valido \_           | Il formato non è valido.                                                                         |
| \_ \_ risorsa INsufficiente \_ SCESTATUS | Memoria insufficiente.                                                                    |
| \_accesso \_ negato a SCESTATUS        | Il chiamante non dispone di privilegi sufficienti per completare questa azione.                          |
| \_eliminazione del cant SCESTATUS \_          | La funzione non può eliminare l'elemento specificato.                                                   |
| \_overflow prefisso \_ SCESTATUS      | Si è verificato un overflow del prefisso.                                                                      |
| SCESTATUS \_ altro \_ errore          | Si è verificato un errore non specificato.                                                               |
| SCESTATUS \_ già \_ in esecuzione      | Il servizio è già in esecuzione.                                                                  |
| il \_ servizio SCESTATUS \_ non è \_ supportato | Il servizio specificato non è supportato.                                                          |
| \_mod SCESTATUS \_ non \_ trovato       | Impossibile trovare o caricare una DLL del motore allegati elencata nel registro di sistema.      |
| \_eccezione SCESTATUS \_ nel \_ Server | Si è verificata un'eccezione nel server.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valori restituiti della funzione di criteri LSA

La maggior parte delle funzioni di criteri dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) restituisce un valore NTSTATUS per indicare l'esito positivo o negativo. I vari valori NTSTATUS sono definiti in ntstatus. h, che viene distribuito con Microsoft Windows Driver Development Kit (DDK).

Per convertire un valore restituito di NTSTATUS in un codice di errore di Windows, usare la funzione [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) .

Nella tabella seguente sono elencati i valori NTSTATUS che possono essere restituiti da qualsiasi funzione LSA. Le sezioni relative al valore restituito per alcune funzioni LSA elencano codici di errore aggiuntivi che la funzione potrebbe restituire. Questa tabella elenca anche il codice di errore di Windows corrispondente a ogni valore di NTSTATUS.



| Codice NTSTATUS (codice di errore di Windows)                                        | Significato                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| STATO \_ riuscita (errore \_ riuscita)<br/>                               | La funzione è stata completata.                                                                                                            |
| \_accesso stato \_ negato ( \_ accesso errore \_ negato)<br/>                 | Il chiamante non dispone dell'accesso appropriato per completare l'operazione.                                                                  |
| STATO \_ risorse insufficienti \_ (errore \_ senza \_ risorse di sistema \_ )<br/> | Risorse di sistema insufficienti (ad esempio memoria per allocare buffer) per completare la chiamata.                                        |
| STATO \_ \_ errore database interno \_ (errore \_ interno \_ database errore \_ )<br/>       | Il database LSA contiene un'incoerenza interna.                                                                                    |
| STATO \_ handle non valido \_ ( \_ errore \_ handle non valido)<br/>               | Indica che un oggetto o un handle RPC non è valido nel [*contesto*](/windows/desktop/SecGloss/c-gly) utilizzato.     |
| stato \_ Server non valido \_ \_ (errore \_ \_ stato server non valido \_ )<br/> | Indica che il server LSA è attualmente disabilitato.                                                                                         |
| STATO \_ parametro non valido \_ ( \_ parametro errore non valido \_ )<br/>         | Uno dei parametri non è valido.                                                                                                     |
| STATO \_ senza \_ privilegi di questo tipo \_ (errore \_ senza \_ tale \_ privilegio)<br/>       | Indica che il privilegio specificato non esiste.                                                                                         |
| \_nome oggetto \_ stato \_ non \_ trovato (file di errore \_ \_ non \_ trovato)<br/>     | Impossibile trovare un oggetto nel database dei criteri LSA. È possibile che l'oggetto sia stato specificato per SID o per nome, a seconda del tipo. |
| LO stato non è \_ riuscito (errore \_ gen errore \_ )<br/>                     | Errore generico, ad esempio errore di connessione RPC.                                                                                        |



 

 


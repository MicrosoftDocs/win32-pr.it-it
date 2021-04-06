---
title: Informazioni sugli errori estesi
description: Le informazioni estese sugli errori sono una matrice di record, ciascuno dei quali indica il passaggio del codice di errore attraverso un particolare livello del sistema o dell'applicazione.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2918caa446f7cee9c4eaa609a5713c9cb385e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045075"
---
# <a name="understanding-extended-error-information"></a>Informazioni sugli errori estesi

Le informazioni estese sugli errori sono una matrice di record, ciascuno dei quali indica il passaggio del codice di errore attraverso un particolare livello del sistema o dell'applicazione. Se si verifica un errore in un computer C, così come viene chiamato dal computer B, che a sua volta viene chiamato dal computer A, il tempo di esecuzione RPC nel computer C genera uno o più record che descrivono l'errore e li passa al computer B. il computer B può aggiungere uno o più record all'inizio della catena esistente e passa la catena completa a un. Un oggetto può aggiungere uno o più record, visualizzare o registrare le informazioni. In sostanza, la catena di errori estesi rappresenta la cronologia dell'errore.

Le informazioni estese sugli errori non sostituiscono il codice di errore ( \_ \_ \* codice di stato RPC). Indipendentemente dalla quantità o dall'eventuale generazione di informazioni sugli errori estesi, il codice di errore rimane invariato.

Ogni record di informazioni sugli errori estesi contiene quanto segue. Per ulteriori informazioni, vedere [**\_ \_ \_ informazioni sugli errori estesi RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) :

-   ComputerName: nome DNS non qualificato del computer in cui ha avuto origine l'errore. Solo i record sui limiti del computer contengono queste informazioni. Ad esempio, nello scenario descritto in precedenza con i computer A, B e C, il ComputerName viene definito per i campi seguenti:

    | Registra                            | Campo ComputerName |
    |-----------------------------------|--------------------|
    | Record \# 1 generato dal computer C | \-                 |
    | Record \# 2 generato dal computer C | \-                 |
    | Record \# 3 generato dal computer C | C                  |
    | Record \# 1 generato dal computer B | \-                 |
    | Record \# 2 generato dal computer B | \-                 |
    | Record \# 3 generato dal computer B | B                  |
    | Record \# 1 generato dal computer A | \-                 |
    | Record \# 2 generato dal computer A | \-                 |
    | Record \# 3 generato dal computer A | \-                 |
    | Inizio della catena                 |                    |

    

     

<!-- -->

-   ProcessID-identificatore del processo che ha generato l'errore.
-   TimeStamp: ora in cui si è verificato l'errore, espresso in formato UTC.
-   Generazione del componente: definizione del codice integer del componente logico che ha generato l'errore. Sono attualmente definiti i componenti seguenti:

    | Codice | Nome              | Descrizione                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Applicazione       | Componente proprietario della routine di gestione per la chiamata RPC specifica                                                                                                                  |
    | 2    | Runtime           | Tempo di esecuzione RPC                                                                                                                                                                      |
    | 3    | Provider di sicurezza | Provider di sicurezza per questa chiamata.                                                                                                                                                  |
    | 4    | NPFS              | NPFS file system                                                                                                                                                                  |
    | 5    | RDR               | Redirector                                                                                                                                                                        |
    | 6    | NNOME MP               | Sistema di named pipe. Può essere NPFS o RDR, ma in molti casi il tempo di esecuzione RPC non sa chi ha eseguito l'operazione richiesta e in questi casi viene restituito NMP. |
    | 7    | IO                | Sistema i/o o driver utilizzato dal sistema IO. Può essere NPFS, RDR o un provider Winsock.                                                                                 |
    | 8    | Winsock           | Provider Winsock                                                                                                                                                                  |
    | 9    | Codice authz        | API di autorizzazione.                                                                                                                                                               |
    | 10   | LPC               | Funzione di chiamata della procedura locale.                                                                                                                                                    |

    

     

<!-- -->

-   Stato: codice di errore generato o restituito dal livello
-   DetectionLocation: numero univoco che identifica la posizione del codice in cui è stato rilevato l'errore. Questo campo è associato al codice e cambierà dalla versione alla versione. Verrà pubblicato un elenco separato dei percorsi di rilevamento più comunemente rilevati.
-   Flags: flag che specificano le informazioni sul record. I flag attualmente definiti sono EEInfoPreviousRecordsMissing e EEInfoNextRecordsMissing, corrispondenti rispettivamente ai valori numerici 1 e 2. Se è impostato EEInfoPreviousRecordsMissing, uno o più record prima di tale record risultano mancanti. Se è impostato EEInfoNextRecordsMissing, uno o più record dopo tale record risultano mancanti. Per una descrizione del motivo per cui è possibile che i record siano mancanti, vedere [affidabilità delle informazioni estese sugli errori](reliability-of-extended-error-information.md).
-   Fino a quattro parametri di errore. Un parametro error è una struttura VARIANT leggera che fornisce informazioni aggiuntive sull'errore. Le informazioni aggiuntive dipendono dall'errore e dalla posizione di rilevamento. I parametri possono essere di tipo stringa ANSI (LPSTR), stringa Unicode (LPWSTR), valore Long (Long), short value (Short), Pointer (Int64) o None.

 

 





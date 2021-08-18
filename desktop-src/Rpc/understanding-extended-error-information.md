---
title: Informazioni sugli errori estesi
description: Le informazioni estese sugli errori sono una matrice di record, ognuno dei quali indica il passaggio del codice di errore attraverso un livello specifico nel sistema o nell'applicazione.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e003214198b06f04479ec4c1a8d23cb1acedafda49eefcf2880741416901323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011059"
---
# <a name="understanding-extended-error-information"></a>Informazioni sugli errori estesi

Le informazioni estese sugli errori sono una matrice di record, ognuno dei quali indica il passaggio del codice di errore attraverso un livello specifico nel sistema o nell'applicazione. Se si verifica un errore in un computer C, come viene chiamato dal computer B, che a sua volta viene chiamato dal computer A, il tempo di esecuzione RPC nel computer C genera uno o più record che descrivono l'errore e li passa al computer B. Il computer B può aggiungere uno o più record alla testa della catena esistente,  e passa l'intera catena ad A. Un oggetto può aggiungere uno o più record e visualizzare o registrare le informazioni. In sostanza, quindi, la catena di errori estesa rappresenta la cronologia dell'errore.

Le informazioni sull'errore estese non sostituiscono il codice di errore (codice di \_ stato RPC \_ \* S). Indipendentemente dalla quantità o dalla generazione delle informazioni sugli errori estese, il codice di errore rimane invariato.

Ogni record di informazioni sugli errori esteso contiene quanto segue. Per altre informazioni, vedere RPC EXTENDED ERROR INFO (INFORMAZIONI [**\_ \_ SULL'ERRORE \_ ESTESO RPC):**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)

-   ComputerName: nome DNS non completo del computer in cui ha avuto origine l'errore. Queste informazioni sono disponibili solo per i record nei limiti del computer. Ad esempio, nello scenario descritto in precedenza con i computer A, B e C, computerName viene definito per i campi seguenti:

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
    | Testa della catena                 |                    |

    

     

<!-- -->

-   ProcessID: identificatore del processo che ha generato l'errore.
-   TimeStamp: ora in cui si è verificato l'errore, espresso in formato UTC.
-   Generazione del componente: definizione di codice intero del componente logico che ha generato l'errore. I componenti seguenti sono attualmente definiti:

    | Codice | Nome              | Descrizione                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Applicazione       | Componente proprietario della routine di gestione per la chiamata RPC specifica                                                                                                                  |
    | 2    | Runtime           | Fase di esecuzione RPC                                                                                                                                                                      |
    | 3    | Provider di sicurezza | Provider di sicurezza per questa chiamata.                                                                                                                                                  |
    | 4    | NPFS              | Il file system NPFS                                                                                                                                                                  |
    | 5    | Rdr               | The Redirector                                                                                                                                                                        |
    | 6    | Nmp               | Il named pipe sistema. Può trattarsi di NPFS o RDR, ma in molti casi il tempo di esecuzione RPC non sa chi ha eseguito l'operazione richiesta e in questi casi viene restituito NMP. |
    | 7    | IO                | Il sistema di I/O o un driver usato dal sistema di I/O. Può trattarsi di NPFS, RDR o di un provider Winsock.                                                                                 |
    | 8    | Winsock           | Provider Winsock                                                                                                                                                                  |
    | 9    | Codice Authz        | API di autorizzazione.                                                                                                                                                               |
    | 10   | Lpc               | Funzione local procedure call.                                                                                                                                                    |

    

     

<!-- -->

-   Stato: codice di errore generato o restituito dal livello
-   DetectionLocation: numero univoco che identifica la posizione del codice in cui è stato rilevato l'errore. Questo campo è associato al codice e cambierà da versione a versione. Verrà pubblicato un elenco separato dei percorsi di rilevamento più comunemente rilevati.
-   Flag: flag che specificano informazioni sul record. I flag attualmente definiti sono EEInfoPreviousRecordsMissing ed EEInfoNextRecordsMissing, corrispondenti rispettivamente ai valori numerici 1 e 2. Se EEInfoPreviousRecordsMissing è impostato, uno o più record prima di tale record non sono presenti. Se EEInfoNextRecordsMissing è impostato, uno o più record dopo tale record non sono presenti. Per una descrizione dei motivi per cui i record potrebbero mancare, vedere [Affidabilità delle informazioni sugli errori estesi](reliability-of-extended-error-information.md).
-   Fino a quattro parametri di errore. Un parametro di errore è una struttura di variante leggera che fornisce informazioni aggiuntive sull'errore. Le informazioni aggiuntive dipendono dall'errore e dalla posizione di rilevamento. I parametri possono essere di tipo stringa ANSI (LPSTR), stringa Unicode (LPWSTR), valore lungo (long), valore breve (short), puntatore (int64) o nessuno.

 

 





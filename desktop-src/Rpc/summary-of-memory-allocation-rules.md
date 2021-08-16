---
title: Riepilogo delle regole di allocazione della memoria
description: La tabella seguente riepiloga le regole chiave relative all'allocazione di memoria.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec50632693ad0df7ff44aa1d2a9a2760b07a2ed1b72a13ac5dc33294569c3484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924702"
---
# <a name="summary-of-memory-allocation-rules"></a>Riepilogo delle regole di allocazione della memoria

La tabella seguente riepiloga le regole chiave relative all'allocazione di memoria.



| Elemento MIDL                                                                                                                                           | Descrizione                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Puntatori di riferimento \[ [di primo](/windows/desktop/Midl/ref) \] livello                                                                                                                | Devono essere puntatori non Null.                                                                                                                                            |
| Valore restituito della funzione                                                                                                                                  | La nuova memoria viene sempre allocata per i valori restituiti del puntatore.                                                                                                             |
| \[[unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), out \] pointer                                                                   | Non consentito da MIDL.                                                                                                                                                  |
| Non-top-level \[ [unique](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), in, out \] pointer that changes from null to non-null | Gli stub client allocano nuova memoria al client al ritorno.                                                                                                                 |
| Puntatore out \[ [univoco non](/windows/desktop/Midl/unique)di primo livello, [in](/windows/desktop/Midl/in), che cambia da non Null a [](/windows/desktop/Midl/out-idl) \] Null                                 | La memoria è orfana nel client. l'applicazione client è responsabile della rimozione della memoria e della prevenzione delle perdite.                                                              |
| ptr non di primo \[ [](/windows/desktop/Midl/ptr)livello, [in](/windows/desktop/Midl/in), [puntatore out](/windows/desktop/Midl/out-idl) \] che cambia da non Null a Null                                       | La memoria sarà orfana nel client se non è stato specificato un alias. In questo caso, l'applicazione client è responsabile della rimozione e della prevenzione delle perdite di memoria.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Puntatori                                                                                                                           | Il livello dell'applicazione client viene in genere allocato.                                                                                                                           |
| Puntatore non Null \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \]                                                                                                | Gli stub tentano di scrivere nell'archiviazione esistente nel client. Se **\[ la stringa \]** e le dimensioni aumentano oltre le dimensioni allocate nel client, al ritorno si verifica un errore di Criteri di gruppo. |



 

Nella tabella seguente sono riepilogati gli effetti dei principali attributi IDL e ACF sulla gestione della memoria.



| Funzionalità MIDL                                                                   | Problemi relativi al client                                                                                                                                  | Problemi del server                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocare](/windows/desktop/Midl/allocate)(nodo \_ singolo), \] \[ allocare (tutti i \_ nodi)\]         | Determina se vengono effettuate una o più chiamate alle funzioni di memoria.                                                                         | Uguale al client, ad eccezione del fatto che la memoria privata può essere spesso usata per allocare (nodo singolo) i dati \_ in e \[ in \] \[ \] uscita.               |
| \[allocate(free) \] o \[ allocate(don't \_ free)\]                                 | (Nessuno; influisce sul server.)                                                                                                                        | Determina se la memoria nel server viene liberata dopo ogni chiamata di procedura remota.                                            |
| gli attributi \[ [della matrice max \_ sono](/windows/desktop/Midl/max-is) \] e size \[ [ \_ è](/windows/desktop/Midl/size-is)\] | (Nessuno; influisce sul server.)                                                                                                                        | Determina le dimensioni della memoria da allocare.                                                                                    |
| \[[numero di \_ byte](/windows/desktop/Midl/byte-count)\]                                            | Il client deve allocare buffer. non allocato o liberato dagli stub client.                                                                           | L'attributo del parametro ACF determina le dimensioni del buffer allocato nel server.                                                        |
| \[[abilitare \_ l'allocazione](/windows/desktop/Midl/enable-allocate)\]                                  | In genere, nessuno. Tuttavia, il client potrebbe usare un ambiente di gestione della memoria diverso.                                                     | Il server usa un ambiente di gestione della memoria diverso. [**RpcSmAllocate deve**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) essere usato per le allocazioni. |
| \[[in](/windows/desktop/Midl/in) \] Attributo                                                    | Applicazione client responsabile dell'allocazione della memoria per i dati.                                                                                 | Allocato nel server da stub.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Attributo                                             | Allocato nel client da stub.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] Il puntatore -only deve essere \[ [un puntatore ref,](/windows/desktop/Midl/ref) \] allocato nel server da stub.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Attributo                                                 | La memoria a cui fa riferimento il puntatore deve essere allocata dall'applicazione client.                                                                          | Puntatori di riferimento di primo e primo livello gestiti da stub.                                                                |
| \[[univoco](/windows/desktop/Midl/unique) \] Attributo                                           | Da non Null a Null può comportare la memoria orfana. Da null a non Null fa in modo che lo stub del client [chiami midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). | Influisce sul client.                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] Attributo                                                 | \[Vedere [univoco.)](/windows/desktop/Midl/unique) \]                                                                                                              | \[Vedere [univoco.)](/windows/desktop/Midl/unique) \]                                                                                             |



 

 

 
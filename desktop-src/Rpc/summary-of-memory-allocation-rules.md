---
title: Riepilogo delle regole di allocazione della memoria
description: Nella tabella seguente sono riepilogate le regole principali relative all'allocazione di memoria.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118118"
---
# <a name="summary-of-memory-allocation-rules"></a>Riepilogo delle regole di allocazione della memoria

Nella tabella seguente sono riepilogate le regole principali relative all'allocazione di memoria.



| Elemento MIDL                                                                                                                                           | Descrizione                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[Puntatori [ref](/windows/desktop/Midl/ref) di primo livello \]                                                                                                                | Deve essere puntatori non null.                                                                                                                                            |
| Valore restituito dalla funzione                                                                                                                                  | La nuova memoria viene sempre allocata per i valori restituiti del puntatore.                                                                                                             |
| \[[Unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), \] puntatore out                                                                   | Non consentito da MIDL.                                                                                                                                                  |
| Valore univoco non di primo livello \[ [](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), in, \] puntatore out che cambia da null a non null | Gli stub client allocano la nuova memoria sul client alla restituzione.                                                                                                                 |
| Puntatore non di primo livello \[ [univoco](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] che cambia da non null a null                                 | La memoria è orfana sul client; l'applicazione client è responsabile della liberazione della memoria e della prevenzione delle perdite.                                                              |
| Puntatore non di primo livello \[ [](/windows/desktop/Midl/ptr), [in](/windows/desktop/Midl/in), puntatore [out](/windows/desktop/Midl/out-idl) \] che cambia da non null a null                                       | La memoria sarà orfana sul client se non è associato a un alias; in questo caso l'applicazione client è responsabile della liberazione e della prevenzione delle perdite di memoria.                             |
| \[[riferimento](/windows/desktop/Midl/ref) \] puntatori                                                                                                                           | Il livello applicazione client in genere alloca.                                                                                                                           |
| Non null \[ [in](/windows/desktop/Midl/in), puntatore [out](/windows/desktop/Midl/out-idl) \]                                                                                                | Gli stub tentano di scrivere nella risorsa di archiviazione esistente nel client. Se la **\[ stringa \]** e le dimensioni aumentano oltre le dimensioni allocate nel client, si verificherà un errore di GP al ritorno. |



 

Nella tabella seguente sono riepilogati gli effetti degli attributi IDL e ACF chiave sulla gestione della memoria.



| Funzionalità MIDL                                                                   | Problemi relativi al client                                                                                                                                  | Problemi del server                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[alloca](/windows/desktop/Midl/allocate)( \_ nodo singolo) \] , \[ alloca (tutti i \_ nodi)\]         | Determina se vengono effettuate una o più chiamate alle funzioni di memoria.                                                                         | Come per il client, ad eccezione della memoria privata, spesso è possibile usare per allocare ( \_ nodo singolo) \[ \] \[ i dati in uscita e in \] .               |
| \[alloca (gratuito) \] o \[ alloca (non \_ disponibile)\]                                 | (Nessuna; influisca sul server).                                                                                                                        | Determina se la memoria nel server viene liberata dopo ogni chiamata di procedura remota.                                            |
| attributi di matrice \[ [Max \_ è](/windows/desktop/Midl/max-is) \] e \[ [dimensioni \_ ](/windows/desktop/Midl/size-is)\] | (Nessuna; influisca sul server).                                                                                                                        | Determina la dimensione della memoria da allocare.                                                                                    |
| \[[ \_ conteggio byte](/windows/desktop/Midl/byte-count)\]                                            | Il client deve allocare il buffer; non allocata o liberata dagli stub client.                                                                           | L'attributo del parametro ACF determina la dimensione del buffer allocato nel server.                                                        |
| \[[Abilita \_ allocazione](/windows/desktop/Midl/enable-allocate)\]                                  | In genere, None. Tuttavia, il client potrebbe usare un ambiente di gestione della memoria diverso.                                                     | Il server utilizza un ambiente di gestione della memoria diverso. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) deve essere utilizzato per le allocazioni. |
| \[[in](/windows/desktop/Midl/in) \] attributo                                                    | Applicazione client responsabile dell'allocazione della memoria per i dati.                                                                                 | Allocato nel server da stub.                                                                                                 |
| \[in [uscita](/windows/desktop/Midl/out-idl) \] attributo                                             | Allocata nel client da stub.                                                                                                                  | \[in [uscita](/windows/desktop/Midl/out-idl) \] -solo il puntatore deve essere un \[ [](/windows/desktop/Midl/ref) \] puntatore Ref, allocato nel server da stub.                       |
| \[[riferimento](/windows/desktop/Midl/ref) \] attributo                                                 | La memoria a cui fa riferimento il puntatore deve essere allocata dall'applicazione client.                                                                          | Puntatori di riferimento di primo livello e di primo livello gestiti da stub.                                                                |
| \[[univoco](/windows/desktop/Midl/unique) \] attributo                                           | La memoria orfana può causare un valore diverso da null. da null a non null fa sì che lo stub client chiami l' [ \_ utente MIDL \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). | (Influiscono sul client).                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] attributo                                                 | (Vedere \[ [univoco](/windows/desktop/Midl/unique) \] ).                                                                                                              | (Vedere \[ [univoco](/windows/desktop/Midl/unique) \] ).                                                                                             |



 

 

 
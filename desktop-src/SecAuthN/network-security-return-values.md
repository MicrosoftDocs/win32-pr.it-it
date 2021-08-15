---
description: Restituisce i valori che un provider di rete può impostare.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valori restituiti dalla sicurezza di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40fd8e6e21d9e7671c1e7b9c3d008978628e28cb0fcb01c3df56359144e72e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921300"
---
# <a name="network-security-return-values"></a>Valori restituiti dalla sicurezza di rete

I valori restituiti che un provider di rete può impostare includono i codici di errore seguenti.



| Codici errore         | Descrizione                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ SUCCESS         | Funzione completata.                                                                                                                                                                                                                                                                                                                 |
| WN \_ NON \_ SUPPORTATO  | La funzione non è supportata in questo provider di rete.                                                                                                                                                                                                                                                                                 |
| ERRORE WN \_ \_ NET      | Si è verificato un errore di rete sconosciuto.                                                                                                                                                                                                                                                                                                       |
| WN \_ MORE \_ DATA      | Il buffer di dati passato non è sufficiente per contenere tutti i dati disponibili.                                                                                                                                                                                                                                                         |
| PUNTATORE WN \_ \_ NON VALIDO    | Durante la chiamata di funzione è stato specificato un puntatore non valido.                                                                                                                                                                                                                                                                     |
| VALORE WN \_ \_ NON VALIDO      | Durante la chiamata di funzione è stato specificato un valore numerico non valido.                                                                                                                                                                                                                                                               |
| WN \_ PASSWORD \_ NON VALIDA   | È stata specificata una password non corretta.                                                                                                                                                                                                                                                                                                    |
| ACCESSO \_ WN \_ NEGATO  | Il chiamante non dispone di autorizzazioni sufficienti per completare l'operazione.                                                                                                                                                                                                                                                              |
| FUNZIONE WN \_ \_ OCCUPATA  | Questa funzione non può essere rientrata ed è attualmente in uso oppure il provider è ancora in fase di inizializzazione e non è ancora pronto per essere chiamato. Il provider deve restituire questo codice di errore solo se sarà disponibile. Questo codice restituito viene passato dalla MPR al chiamante ed è probabile che il chiamante ritenta.<br/> |
| ERRORE DI \_ WINDOWS \_ WN  | Una funzione obbligatoria non è riuscita.                                                                                                                                                                                                                                                                                                             |
| WN \_ BAD \_ USER       | È stato specificato un nome utente non valido.                                                                                                                                                                                                                                                                                            |
| MEMORIA \_ INSUFFICIENTE \_ \_ | Memoria insufficiente per completare l'operazione.                                                                                                                                                                                                                                                                                 |
| WN \_ NON \_ CONNESSO  | Il dispositivo non viene reindirizzato.                                                                                                                                                                                                                                                                                                           |
| FILE APERTI \_ WN \_     | Impossibile annullare la connessione perché i file sono ancora aperti.                                                                                                                                                                                                                                                                      |
| WN \_ BAD \_ NETNAME    | Il nome di rete non è valido.                                                                                                                                                                                                                                                                                                          |



 

 

 





---
description: Valori restituiti che possono essere impostati da un provider di rete.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valori restituiti dalla sicurezza di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a362fde712d2a44565894aceb9d85172e488b53a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968087"
---
# <a name="network-security-return-values"></a>Valori restituiti dalla sicurezza di rete

I valori restituiti che un provider di rete può impostare includono i codici di errore seguenti.



| Codici errore         | Descrizione                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_operazione riuscita         | Funzione completata.                                                                                                                                                                                                                                                                                                                 |
| \_non \_ supportato  | La funzione non è supportata in questo provider di rete.                                                                                                                                                                                                                                                                                 |
| \_errore della rete \_      | Si è verificato un errore di rete sconosciuto.                                                                                                                                                                                                                                                                                                       |
| \_altri \_ dati      | Il buffer di dati passato non è sufficiente per contenere tutti i dati disponibili.                                                                                                                                                                                                                                                         |
| \_puntatore non valido \_    | Un puntatore non valido è stato specificato durante la chiamata di funzione.                                                                                                                                                                                                                                                                     |
| \_valore non valido \_      | Durante la chiamata di funzione è stato specificato un valore numerico non valido.                                                                                                                                                                                                                                                               |
| \_password non valida \_   | È stata specificata una password errata.                                                                                                                                                                                                                                                                                                    |
| \_accesso \_ negato  | Il chiamante non dispone di autorizzazioni sufficienti per completare l'operazione.                                                                                                                                                                                                                                                              |
| \_funzione. \_  | Questa funzione non può essere rientrata ed è attualmente in uso oppure il provider è ancora in fase di inizializzazione e non è ancora pronto per essere chiamato. Il provider deve restituire questo codice di errore solo se sarà disponibile. Questo codice restituito viene passato da MPR al chiamante ed è probabile che il chiamante ritenti.<br/> |
| \_errore di Windows \_  | Funzione obbligatoria non riuscita.                                                                                                                                                                                                                                                                                                             |
| \_utente non valido \_       | È stato specificato un nome utente non valido.                                                                                                                                                                                                                                                                                            |
| - \_ \_ \_ memoria insufficiente | Memoria insufficiente per completare l'operazione.                                                                                                                                                                                                                                                                                 |
| \_non \_ connesso  | Il dispositivo non viene reindirizzato.                                                                                                                                                                                                                                                                                                           |
| \_Apri \_ file aperti     | Impossibile annullare la connessione perché i file sono ancora aperti.                                                                                                                                                                                                                                                                      |
| \_NETNAME non valido \_    | Il nome di rete non è valido.                                                                                                                                                                                                                                                                                                          |



 

 

 





---
title: Funzioni api WebDAV
description: Nell'API WebDAV vengono usate le funzioni seguenti.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401f527bcd98f86f8116df5b25ba1ea71e0f432e19dc89eae00582a2a0b4865e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995041"
---
# <a name="webdav-api-functions"></a>Funzioni api WebDAV

Nell'API WebDAV vengono usate le funzioni seguenti.



| Funzione                                                             | Descrizione                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Crea una connessione sicura a un server WebDAV o a un file o a una directory remota in un server WebDAV.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Il client WebDAV chiama la funzione di callback [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) definita dall'applicazione per richiedere le credenziali all'utente.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Chiude tutte le connessioni a un server WebDAV o a un file o a una directory remota in un server WebDAV.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Chiude una connessione creata usando la [**funzione DavAddConnection.**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Scarica i dati dalla versione locale di un file remoto al server WebDAV.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Il client WebDAV chiama la funzione di callback [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) definita dall'applicazione per liberare le informazioni sulle credenziali recuperate dalla funzione di callback [*DavAuthCallback.*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Recupera le informazioni estese sul codice di errore restituite dal server WebDAV per l'operazione di I/O non riuscita precedente.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Converte il percorso UNC specificato in un percorso HTTP equivalente.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Restituisce il proprietario del blocco file per un file bloccato in un server WebDAV.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Converte il percorso HTTP specificato in un percorso UNC equivalente.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Invalida il contenuto della cache locale per un file remoto in un server WebDAV.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registra una funzione di callback definita dall'applicazione che il client WebDAV può usare per richiedere le credenziali all'utente.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Annulla la registrazione di una funzione di callback registrata utilizzata dal client WebDAV per richiedere le credenziali all'utente.                                                                                                                            |



 

 

 





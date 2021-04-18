---
title: Funzioni API WebDAV
description: Nell'API WebDAV vengono usate le funzioni seguenti.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1917cd6ebb64470eec6fde9188cc39341142fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298763"
---
# <a name="webdav-api-functions"></a>Funzioni API WebDAV

Nell'API WebDAV vengono usate le funzioni seguenti.



| Funzione                                                             | Descrizione                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Crea una connessione sicura a un server WebDAV o a un file o a una directory remota in un server WebDAV.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Il client WebDAV chiama la funzione di callback [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) definita dall'applicazione per richiedere le credenziali all'utente.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Chiude tutte le connessioni a un server WebDAV o a un file o a una directory remota in un server WebDAV.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Chiude una connessione creata tramite la funzione [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) .                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Scarica i dati dalla versione locale di un file remoto al server WebDAV.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Il client WebDAV chiama la funzione di callback [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) definita dall'applicazione per liberare le informazioni sulle credenziali recuperate dalla funzione di callback [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) . |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Recupera le informazioni sul codice di errore estese restituite dal server WebDAV per le operazioni di I/O non riuscite precedenti.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Converte il percorso UNC specificato in un percorso HTTP equivalente.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Restituisce il proprietario del blocco di file per un file bloccato in un server WebDAV.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Converte il percorso HTTP specificato in un percorso UNC equivalente.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Invalida il contenuto della cache locale per un file remoto in un server WebDAV.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registra una funzione di callback definita dall'applicazione che il client WebDAV può utilizzare per richiedere le credenziali all'utente.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Annulla la registrazione di una funzione di callback registrata che il client WebDAV utilizza per richiedere le credenziali all'utente.                                                                                                                            |



 

 

 





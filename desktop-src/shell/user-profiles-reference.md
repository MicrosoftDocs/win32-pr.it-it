---
description: Gli elementi API seguenti vengono usati con i profili utente.
title: Informazioni di riferimento sui profili utente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967831"
---
# <a name="user-profiles-reference"></a>Informazioni di riferimento sui profili utente

Gli elementi API seguenti vengono usati con i profili utente.

## <a name="functions"></a>Funzioni



| Funzione                                                                   | Descrizione                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Recupera le variabili di ambiente per l'utente specificato.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Crea un nuovo profilo utente. (Windows Vista e versioni successive.                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Elimina il profilo utente e tutte le impostazioni relative all'utente dal computer specificato.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Libera le variabili di ambiente create [**dalla funzione CreateEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Espande la stringa di origine usando il blocco di ambiente stabilito per l'utente specificato.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Recupera il percorso della radice del profilo Tutti gli utenti.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Recupera il percorso della radice del profilo Utente predefinito.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Recupera il percorso della directory radice in cui sono archiviati tutti i profili utente.                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Recupera il tipo di profilo caricato per l'utente corrente.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Recupera il percorso della directory radice del profilo dell'utente specificato.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Carica il profilo dell'utente specificato.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Scarica un profilo utente caricato dalla funzione [**LoadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)          |



 

La [**funzione CreateUserProfileEx**](createuserprofileex.md) non è supportata.

## <a name="structures"></a>Strutture



| Struttura                          | Descrizione                                |
|------------------------------------|--------------------------------------------|
| [**Profileinfo**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Contiene informazioni su un profilo utente. |



 

 

 




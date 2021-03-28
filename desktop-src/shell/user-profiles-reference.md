---
description: I seguenti elementi API vengono usati con i profili utente.
title: Riferimento ai profili utente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980711"
---
# <a name="user-profiles-reference"></a>Riferimento ai profili utente

I seguenti elementi API vengono usati con i profili utente.

## <a name="functions"></a>Funzioni



| Funzione                                                                   | Descrizione                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Recupera le variabili di ambiente per l'utente specificato.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Crea un nuovo profilo utente. (Solo Windows Vista e versioni successive).                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Elimina il profilo utente e tutte le impostazioni relative agli utenti dal computer specificato.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Libera le variabili di ambiente create dalla funzione [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Espande la stringa di origine usando il blocco dell'ambiente stabilito per l'utente specificato.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Recupera il percorso della radice del profilo All Users.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Recupera il percorso della radice del profilo utente predefinito.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Recupera il percorso della directory radice in cui sono archiviati tutti i profili utente.                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Recupera il tipo di profilo caricato per l'utente corrente.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Recupera il percorso della directory radice del profilo utente specificato.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Carica il profilo utente specificato.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Scarica un profilo utente caricato dalla funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .          |



 

La funzione [**CreateUserProfileEx**](createuserprofileex.md) non è supportata.

## <a name="structures"></a>Strutture



| Struttura                          | Descrizione                                |
|------------------------------------|--------------------------------------------|
| [**PROFILEINFO**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Contiene informazioni su un profilo utente. |



 

 

 




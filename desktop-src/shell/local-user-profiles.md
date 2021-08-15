---
description: Il sistema crea automaticamente un profilo utente locale per ogni utente quando l'utente accede al computer per la prima volta. Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.
title: Profili utente locali
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 713adc7db522ff473de42a3ecaa2a1a0671f95ee5f4039f0039a196304c7aa4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220156"
---
# <a name="local-user-profiles"></a>Profili utente locali

Windows sicurezza richiede un profilo utente per ogni account utente in un computer. Il sistema crea automaticamente *un profilo utente locale* per ogni utente quando l'utente accede al computer per la prima volta. Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.

Windows Vista e versioni successive: i profili utente vengono gestiti tramite **l'elemento del Pannello di controllo** Account utente.

Windows 2000 e Windows XP: per copiare o eliminare un profilo utente, selezionare  **Sistema** dal Pannello di controllo, quindi la scheda Avanzate e quindi il **pulsante Impostazioni** nell'area Profilo utente. 

Il profilo dell'utente non viene caricato automaticamente quando l'utente è connesso usando la [**funzione LogonUser.**](/windows/win32/api/winbase/nf-winbase-logonusera) Per caricare un profilo utente a livello di codice, usare la [**funzione LoadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) Per scaricare un profilo utente caricato da **LoadUserProfile,** chiamare la [**funzione UnloadUserProfile.**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)

 

 

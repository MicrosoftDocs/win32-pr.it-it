---
description: Il sistema crea automaticamente un profilo utente locale per ogni utente quando l'utente accede al computer per la prima volta. Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.
title: Profili utente locale
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980015"
---
# <a name="local-user-profiles"></a>Profili utente locale

Per la sicurezza di Windows è necessario un profilo utente per ogni account utente in un computer. Il sistema crea automaticamente un *profilo utente locale* per ogni utente quando l'utente accede al computer per la prima volta. Il sistema gestisce automaticamente le impostazioni per l'ambiente di lavoro di ogni utente in un profilo utente nel computer locale.

Windows Vista e versioni successive: i profili utente vengono gestiti tramite l'elemento del pannello di controllo degli **account utente** .

Windows 2000 e Windows XP: per copiare o eliminare un profilo utente, selezionare **sistema** dal pannello di controllo, quindi la scheda **Avanzate** , quindi il pulsante **Impostazioni** nell'area **profilo utente** .

Il profilo dell'utente non viene caricato automaticamente quando l'utente è connesso tramite la funzione [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Per caricare un profilo utente a livello di codice, usare la funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Per scaricare un profilo utente caricato da **LoadUserProfile**, chiamare la funzione [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 

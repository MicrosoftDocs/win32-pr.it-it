---
description: Se un computer esegue Windows 2000 Server o versione successiva in una rete, gli utenti possono archiviare i profili sul server. Questi profili sono detti profili utente mobili.
title: Profili utente mobili
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979938"
---
# <a name="roaming-user-profiles"></a>Profili utente mobili

Se un computer esegue Windows 2000 Server o versione successiva in una rete, gli utenti possono archiviare i profili sul server. Questi profili sono detti *profili utente mobili*.

I profili utente mobili presentano i vantaggi seguenti:

-   Disponibilità automatica delle risorse. Il profilo univoco di un utente è automaticamente disponibile quando accede a un computer in rete. Non è necessario che gli utenti creino un profilo in ogni computer utilizzato in una rete.
-   Sostituzione e backup semplificati del computer. Quando il computer di un utente deve essere sostituito, può essere sostituito facilmente perché tutte le informazioni sul profilo dell'utente sono gestite separatamente nella rete, indipendentemente da un singolo computer. Quando l'utente accede al nuovo computer per la prima volta, la copia server del profilo dell'utente viene copiata nel nuovo computer.

Il profilo dell'utente non viene caricato automaticamente quando l'utente è connesso tramite la funzione [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Per caricare un profilo utente mobile a livello di codice, usare la funzione [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Per scaricare un profilo utente mobile caricato da **LoadUserProfile**, chiamare la funzione [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 

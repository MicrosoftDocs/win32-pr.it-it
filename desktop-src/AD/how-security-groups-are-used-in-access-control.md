---
title: Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso
description: L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per motivi di sicurezza.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso
- controllo di accesso, gruppi di sicurezza usati in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297732"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Modalità di utilizzo di gruppi di sicurezza nel controllo di accesso

L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per motivi di sicurezza. Il nome dell'utente o del gruppo non viene utilizzato come identificatore univoco all'interno del sistema. Il SID viene archiviato nell'attributo **objectSID** degli oggetti utente e dei gruppi di sicurezza. Il server di Active Directory genera il **objectSID** quando viene creato l'utente o il gruppo. Il sistema garantisce che i SID siano univoci in una foresta. Tenere presente che **objectGUID** è l'identificatore univoco di un utente, di un gruppo o di qualsiasi altro oggetto directory. Il SID viene modificato se un utente o un gruppo viene spostato in un altro dominio; il **objectGUID** rimane invariato.

Quando a un utente o a un gruppo viene assegnata l'autorizzazione per accedere a una risorsa, ad esempio una stampante o una condivisione file, il SID dell'utente o del gruppo viene aggiunto alla voce di controllo di accesso (ACE) che definisce l'autorizzazione concessa nell'elenco di controllo di accesso discrezionale (DACL) della risorsa. In Active Directory Domain Services, ogni oggetto dispone di un attributo **ntSecurityDescriptor** che archivia un DACL che definisce l'accesso a quell'oggetto o gli attributi specifici su tale oggetto. Per ulteriori informazioni sull'impostazione del controllo di accesso per gli oggetti in Active Directory Domain Services, vedere [controllo dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Quando un utente accede a un dominio Windows 2000, il sistema operativo genera un token di accesso. Questo token di accesso viene usato per determinare a quali risorse può accedere l'utente. Il token di accesso utente include i dati seguenti:

-   SID utente.
-   SID di tutti i gruppi di sicurezza globali e universali di cui l'utente è membro.
-   SID di tutti i gruppi di sicurezza globali e universali annidati.

Ogni processo eseguito per conto di questo utente ha una copia di questo token di accesso.

Quando l'utente tenta di accedere alle risorse in un computer, il servizio tramite il quale l'utente accede alla risorsa rappresenterà l'utente creando un nuovo token di accesso in base al token di accesso creato al momento dell'accesso dell'utente. Questo nuovo token di accesso conterrà anche i SID seguenti:

-   SID per tutti i gruppi locali di dominio nel dominio di destinazione di cui l'utente è membro.
-   SID per tutti i gruppi locali del computer nel computer di destinazione di cui l'utente è membro.

Il servizio usa questo nuovo token di accesso per valutare l'accesso alla risorsa. Se un SID nel token di accesso viene visualizzato in tutte le voci ACE del DACL, il servizio fornisce all'utente le autorizzazioni specificate in tali ACE.

 

 





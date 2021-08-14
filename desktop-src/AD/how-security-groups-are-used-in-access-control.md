---
title: Modalità di utilizzo dei gruppi di sicurezza nel controllo di accesso
description: L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per scopi di sicurezza.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Modalità di utilizzo dei gruppi di sicurezza nel controllo di accesso
- controllo di accesso, gruppi di sicurezza usati in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8e14d4d8c371d07619d93f4a6d06318f91e7ec011a4c4fe6d436074ac8ff94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188132"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Modalità di utilizzo dei gruppi di sicurezza nel controllo di accesso

L'ID di sicurezza (SID) è l'identificatore di oggetto dell'utente o del gruppo di sicurezza quando l'utente o il gruppo viene utilizzato per scopi di sicurezza. Il nome dell'utente o del gruppo non viene utilizzato come identificatore univoco all'interno del sistema. Il SID viene archiviato **nell'attributo objectSid** degli oggetti utente e degli oggetti gruppo di sicurezza. Il server Active Directory genera **objectSid** quando viene creato l'utente o il gruppo. Il sistema garantisce che i SID siano univoci in una foresta. Tenere presente che **objectGuid è** l'identificatore univoco di un utente, di un gruppo o di qualsiasi altro oggetto directory. Il SID cambia se un utente o un gruppo viene spostato in un altro dominio. **objectGuid** rimane invariato.

Quando a un utente o a un gruppo viene concessa l'autorizzazione per accedere a una risorsa, ad esempio una stampante o una condivisione file, il SID dell'utente o del gruppo viene aggiunto alla voce di controllo di accesso (ACE) che definisce l'autorizzazione concessa nell'elenco di controllo di accesso discrezionale (DACL) della risorsa. In Active Directory Domain Services, ogni oggetto ha un attributo **nTSecurityDescriptor** che archivia un elenco DACL che definisce l'accesso a tale oggetto o a determinati attributi in tale oggetto. Per altre informazioni sull'impostazione del controllo di accesso sugli oggetti in Active Directory Domain Services, vedere [Controllo dell'accesso](controlling-access-to-objects-in-active-directory-domain-services.md)agli oggetti in Active Directory Domain Services .

Quando un utente accede a un dominio Windows 2000, il sistema operativo genera un token di accesso. Questo token di accesso viene usato per determinare le risorse a cui l'utente può accedere. Il token di accesso utente include i dati seguenti:

-   SID utente.
-   SID di tutti i gruppi di sicurezza globali e universali di cui l'utente è membro.
-   SID di tutti i gruppi di sicurezza globali e universali annidati.

Ogni processo eseguito per conto di questo utente dispone di una copia di questo token di accesso.

Quando l'utente tenta di accedere alle risorse in un computer, il servizio tramite il quale l'utente accede alla risorsa rappresenta l'utente creando un nuovo token di accesso basato sul token di accesso creato all'accesso dell'utente. Questo nuovo token di accesso conterrà anche i SID seguenti:

-   SID per tutti i gruppi locali di dominio nel dominio di destinazione di cui l'utente è membro.
-   SID per tutti i gruppi locali del computer nel computer di destinazione di cui l'utente è membro.

Il servizio usa questo nuovo token di accesso per valutare l'accesso alla risorsa. Se un SID nel token di accesso viene visualizzato in qualsiasi ACE nell'elenco DACL, il servizio concede all'utente le autorizzazioni specificate in tali ACE.

 

 





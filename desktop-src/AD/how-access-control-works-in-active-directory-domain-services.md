---
title: Funzionamento del controllo di accesso in Active Directory Domain Services
description: Il controllo di accesso per gli oggetti Active Directory Domain Services è basato su Windows NT e Windows 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, sicurezza, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f53cdd7b958313b3cb16bc538addc73b42bd0dc917160176422b85c959c8c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188287"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Funzionamento del controllo di accesso in Active Directory Domain Services

Il controllo di accesso per gli oggetti Active Directory Domain Services è basato su Windows NT e Windows 2000. Per altre informazioni e una descrizione dettagliata di questo modello e dei relativi componenti, ad esempio descrittori di sicurezza, token di accesso, SID, ACL ed ACE, vedere Modello di controllo di [accesso](/windows/desktop/SecAuthZ/access-control-model).

I privilegi di accesso per le Active Directory Domain Services in genere vengono concessi tramite l'uso di una voce di controllo di accesso (ACE). Una voce ACE definisce un'autorizzazione di accesso o di controllo per un oggetto per un utente o un gruppo specifico. Un elenco di controllo di accesso (ACL) è la raccolta ordinata di voci di controllo di accesso definite per un oggetto . Un descrittore di sicurezza supporta proprietà e metodi che creano e gestiscono ACL. Per altre informazioni sui modelli di sicurezza, vedere [Security](/windows/desktop/SecAuthZ/access-control) o *Windows 2000 Server Resource Kit.* Questa risorsa potrebbe non essere disponibile in alcune lingue, paesi o aree geografiche.

La struttura di base del modello di sicurezza è la seguente:

-   Descrittore di sicurezza. Ogni oggetto directory ha un proprio descrittore di sicurezza che contiene i dati di sicurezza che proteggono l'oggetto. Il descrittore di sicurezza può contenere un elenco di controllo di accesso discrezionale (DACL). Un dacl contiene un elenco di voci ACE. Ogni ACE concede o nega un set di diritti di accesso a un utente o a un gruppo. I diritti di accesso corrispondono alle operazioni, ad esempio la lettura e la scrittura di proprietà, che possono essere eseguite sull'oggetto.
-   Contesto di sicurezza. Quando si accede a un oggetto directory, l'applicazione specifica le credenziali dell'entità di sicurezza che sta effettuando il tentativo di accesso. Quando vengono autenticate, queste credenziali determinano il contesto di sicurezza dell'applicazione, che include le appartenenze ai gruppi e i privilegi associati all'entità di sicurezza. Per altre informazioni sui contesti di sicurezza, vedere [Contesti di](security-contexts-and-active-directory-domain-services.md)sicurezza e Active Directory Domain Services .
-   Controllo di accesso. Il sistema concede l'accesso a un oggetto solo se il descrittore di sicurezza dell'oggetto concede i diritti di accesso necessari all'entità di sicurezza che tenta l'operazione (o ai gruppi a cui appartiene l'entità di sicurezza).

Nella tabella seguente sono elencate le interfacce ADSI utilizzate per modificare le funzionalità di controllo di accesso di Active Directory Domain Services.



| Interfaccia                                                 | Descrizione                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Utilizzato per leggere e scrivere le proprietà di sicurezza di un oggetto servizio directory. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Consente di gestire ed enumerare tutte le voci ACE per un oggetto servizio directory.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Utilizzato per leggere e scrivere le proprietà ACE.                                    |



 

 

 
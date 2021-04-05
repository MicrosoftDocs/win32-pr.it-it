---
title: Funzionamento del controllo di accesso in Active Directory Domain Services
description: Il controllo di accesso per gli oggetti in Active Directory Domain Services è basato sui modelli di controllo di accesso di Windows NT e Windows 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, sicurezza, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956321"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Funzionamento del controllo di accesso in Active Directory Domain Services

Il controllo di accesso per gli oggetti in Active Directory Domain Services è basato sui modelli di controllo di accesso di Windows NT e Windows 2000. Per altre informazioni e una descrizione dettagliata di questo modello e dei relativi componenti, ad esempio i descrittori di sicurezza, i token di accesso, i SID, gli ACL e le voci ACE, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

I privilegi di accesso per le risorse in Active Directory Domain Services vengono in genere concessi tramite l'utilizzo di una voce di controllo di accesso (ACE). Una voce ACE definisce un'autorizzazione di accesso o controllo per un oggetto per un utente o un gruppo specifico. Un elenco di controllo di accesso (ACL) è la raccolta ordinata di voci di controllo di accesso definite per un oggetto. Un descrittore di sicurezza supporta proprietà e metodi che creano e gestiscono ACL. Per ulteriori informazioni sui modelli di sicurezza, vedere la pagina relativa alla [sicurezza](/windows/desktop/SecAuthZ/access-control) o al *Resource Kit di Windows Server 2000*. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

La struttura di base del modello di sicurezza è la seguente:

-   Descrittore di sicurezza. Ogni oggetto directory dispone di un descrittore di sicurezza che contiene i dati di sicurezza che proteggono l'oggetto. Il descrittore di sicurezza può contenere un elenco di controllo di accesso discrezionale (DACL). Un DACL contiene un elenco di voci ACE. Ogni voce ACE concede o nega un set di diritti di accesso a un utente o a un gruppo. I diritti di accesso corrispondono alle operazioni, ad esempio la lettura e la scrittura delle proprietà, che possono essere eseguite sull'oggetto.
-   Contesto di sicurezza. Quando si accede a un oggetto directory, l'applicazione specifica le credenziali dell'entità di sicurezza che sta effettuando il tentativo di accesso. Una volta autenticate, queste credenziali determinano il contesto di sicurezza dell'applicazione, che include le appartenenze ai gruppi e i privilegi associati all'entità di sicurezza. Per ulteriori informazioni sui contesti di sicurezza, vedere [contesti di sicurezza e Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Controllo di accesso. Il sistema concede l'accesso a un oggetto solo se il descrittore di sicurezza dell'oggetto concede i diritti di accesso necessari all'entità di sicurezza che tenta di eseguire l'operazione o ai gruppi a cui appartiene l'entità di sicurezza.

Nella tabella seguente sono elencate le interfacce ADSI utilizzate per modificare le funzionalità di controllo di accesso di Active Directory Domain Services.



| Interfaccia                                                 | Descrizione                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Utilizzato per leggere e scrivere le proprietà di sicurezza di un oggetto servizio di directory. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Utilizzato per gestire ed enumerare tutte le voci ACE per un oggetto servizio di directory.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Utilizzato per leggere e scrivere le proprietà ACE.                                    |



 

 

 
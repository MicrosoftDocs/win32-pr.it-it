---
title: Sicurezza della partizione di directory applicativa
description: Il modello di controllo di sicurezza e di accesso per le partizioni di directory applicative è identico a quello per le altre partizioni in Active Directory Domain Services.
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- ANNUNCIO sulla sicurezza della partizione di directory applicativa
- Directory dell'applicazione partizioni di Active Directory, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da4ce1b8d4e3604b8e546d79003f4d3719223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956348"
---
# <a name="application-directory-partition-security"></a>Sicurezza della partizione di directory applicativa

Il modello di controllo di sicurezza e di accesso per le partizioni di directory applicative è identico a quello per le altre partizioni in Active Directory Domain Services. Gli utenti normali possono accedere agli oggetti di una partizione di directory applicativa soggetta agli ACL posizionati su tali oggetti. Per ulteriori informazioni, vedere [controllo dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Tuttavia, poiché le partizioni di directory applicative possono estendersi su più domini di sicurezza in un servizio directory, si verifica la questione di interpretare le costanti di stringa SID note relative al dominio nell' [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) della classe di schema di un oggetto al momento della creazione dell'oggetto in una partizione di directory applicativa. Se, ad esempio, "DA" si riferisce al gruppo Domain Administrators, ma in una partizione di directory applicativa non è noto a quale dominio si riferisce il gruppo "DA".

Per risolvere questo problema, l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) di una partizione di directory applicativa dispone di un attributo [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) che contiene il nome distinto del dominio di riferimento per la partizione di directory applicativa. Il sistema di sicurezza utilizza il dominio specificato per interpretare i riferimenti del dominio locale per i descrittori di sicurezza predefiniti associati a oggetti creati nella partizione di directory applicativa. È possibile specificare il dominio di riferimento quando viene creato l'oggetto **crossRef** per una partizione di directory applicativa. Questa operazione richiede, tuttavia, che un oggetto **crossRef** sia già stato creato per la partizione di directory applicativa. Se non viene specificato alcun dominio di riferimento, il sistema imposta automaticamente il dominio di riferimento in base a una delle condizioni seguenti:

-   Se l'elemento padre dell'oggetto partizione di directory applicativa è un'altra partizione di directory applicativa, viene usato l'attributo [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) della partizione di directory dell'applicazione padre per il dominio di riferimento.
-   Se l'oggetto padre è un dominio, tale dominio viene utilizzato per il dominio di riferimento.
-   Se non è presente alcun oggetto padre, per il dominio di riferimento viene usato il dominio radice della foresta.

È inoltre possibile modificare l'attributo **crossRef** nel dominio di riferimento dopo la creazione della partizione, ma questa operazione non è consigliata.

Un problema simile si verifica se un gruppo locale viene specificato in un ACL per un oggetto in una partizione di directory applicativa. In questo caso, l'attributo [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) non può essere utilizzato per interpretare il dominio di riferimento per un gruppo locale. Per evitare questo problema, i gruppi locali non devono essere utilizzati negli ACL degli oggetti partizione di directory applicativa.

 

 
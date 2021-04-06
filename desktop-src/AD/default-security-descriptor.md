---
title: Descrittore di sicurezza predefinito
description: Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descrittore di sicurezza predefinito AD
- descrittori di sicurezza AD, valore predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046529"
---
# <a name="default-security-descriptor"></a>Descrittore di sicurezza predefinito

Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto. Viene specificato nell'attributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) nella definizione dell'oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) nello [schema Active Directory](active-directory-schema.md). Questo descrittore di sicurezza viene usato per fornire la protezione predefinita sull'oggetto se non è stato specificato alcun descrittore di sicurezza durante la creazione dell'oggetto.

> [!Note]  
> Le voci ACE di un descrittore di sicurezza predefinito vengono gestite come se fossero specificate come parte della creazione di un oggetto. Pertanto, le voci ACE predefinite vengono posizionate sopra le voci ACE ereditate e vengono sostituite in base alle esigenze. Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) viene specificato in un formato stringa speciale utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). È possibile usare due funzioni per convertire il formato binario del descrittore di sicurezza in formato stringa e viceversa. Queste funzioni sono:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor ha](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Per ulteriori informazioni e per i descrittori di sicurezza predefiniti delle classi di oggetti predefinite, vedere le pagine di riferimento della classe nel riferimento allo schema Active Directory del [riferimento Active Directory Domain Services](active-directory-domain-services-reference.md).

Per ulteriori informazioni e un esempio di codice per la lettura o la modifica della proprietà [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) di una classe di oggetti, vedere [lettura di defaultSecurityDescriptor per una](reading-the-defaultsecuritydescriptor-for-an-object-class.md) classe di oggetti e [modifica di defaultSecurityDescriptor per una classe di oggetti](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 
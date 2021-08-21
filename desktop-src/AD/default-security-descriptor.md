---
title: Descrittore di sicurezza predefinito
description: Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descrittore di sicurezza predefinito AD
- descrittori di sicurezza AD , impostazione predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed57b775196ad6981a88b5621076d76c61035c4700af25ed3f35703fc9018b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019882"
---
# <a name="default-security-descriptor"></a>Descrittore di sicurezza predefinito

Con Active Directory Domain Services, è anche possibile specificare la sicurezza predefinita per ogni tipo di oggetto. Questo valore viene specificato [**nell'attributo defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) nella definizione [**dell'oggetto classSchema**](/windows/desktop/ADSchema/c-classschema) nello [schema di Active Directory.](active-directory-schema.md) Questo descrittore di sicurezza viene utilizzato per fornire la protezione predefinita per l'oggetto se non è stato specificato alcun descrittore di sicurezza durante la creazione dell'oggetto.

> [!Note]  
> Le voci ACE di un descrittore di sicurezza predefinito vengono gestite come se fossero specificate come parte della creazione dell'oggetto. Di conseguenza, le voci ACE predefinite vengono posizionate prima delle ACE ereditate ed eseguirne l'override in base alle esigenze. Per altre informazioni, vedere [Ordine delle ACE in un dacl.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

 

[**DefaultSecurityDescriptor viene**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) specificato in un formato di stringa speciale usando il linguaggio SDDL [(Security Descriptor Definition Language).](/windows/desktop/SecAuthZ/security-descriptor-definition-language) È possibile usare due funzioni per convertire la forma binaria del descrittore di sicurezza in formato stringa e viceversa. Queste funzioni sono:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Per altre informazioni e per i descrittori di sicurezza predefiniti delle classi di oggetti predefinite, vedere le pagine di riferimento alle classi nella guida di riferimento allo schema di Active Directory [di Active Directory Domain Services riferimento.](active-directory-domain-services-reference.md)

Per altre informazioni e un esempio di codice che legge o modifica la proprietà [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) di una classe di oggetti, vedere Lettura di [defaultSecurityDescriptor](reading-the-defaultsecuritydescriptor-for-an-object-class.md) per una classe di oggetti e Modifica di [defaultSecurityDescriptor](modifying-the-defaultsecuritydescriptor-for-an-object-class.md)per una classe di oggetti .

 

 
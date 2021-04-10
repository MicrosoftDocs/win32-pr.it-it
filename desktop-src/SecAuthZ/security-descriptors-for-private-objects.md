---
description: Per creare un descrittore di sicurezza, un server protetto può utilizzare la stessa procedura utilizzata da un'applicazione per creare un descrittore di sicurezza per un oggetto a protezione diretta.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descrittori di sicurezza per oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966817"
---
# <a name="security-descriptors-for-private-objects"></a>Descrittori di sicurezza per oggetti privati

Per creare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly), un server protetto può utilizzare la stessa procedura utilizzata da un'applicazione per creare un descrittore di sicurezza per un oggetto a protezione diretta. Per il codice di esempio, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md). In alternativa, un'applicazione server protetta può chiamare la funzione [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) per eseguire questa operazione. Se a **BuildSecurityDescriptor** viene fornito un puntatore a un [*descrittore di sicurezza autonomo*](/windows/desktop/SecGloss/s-gly) esistente, verrà compilato il nuovo descrittore di sicurezza con le informazioni ricavate dal descrittore di sicurezza Unito con le nuove informazioni di controllo di accesso passate come parametri nella chiamata di funzione. Il proprietario e il gruppo vengono specificati facoltativamente dalle strutture del [**trustee**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) passate alla funzione. Il descrittore di sicurezza creato da **BuildSecurityDescriptor** è in formato *relativo* .

Inoltre, l'API di Windows fornisce un set di funzioni per unire le informazioni di sicurezza del client con le informazioni ereditate dal descrittore di sicurezza per un oggetto padre o da un descrittore di sicurezza predefinito. Le funzioni [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity), [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)e [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) offrono la possibilità di recuperare le informazioni predefinite da un [*token di accesso*](/windows/desktop/SecGloss/a-gly), supportare l'ereditarietà e modificare parti specifiche del descrittore di sicurezza. Questa operazione può essere utile quando un client crea un oggetto privato in una gerarchia di oggetti protetti. Ad esempio, è possibile usare la funzione **CreatePrivateObjectSecurity** per creare un descrittore di sicurezza che contiene le voci ACE specificate dal client, le voci ACE ereditate da un oggetto padre e il proprietario predefinito dal token di accesso del client di creazione. Mentre [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crea descrittori di sicurezza da informazioni sul controllo di accesso passate alla chiamata di funzione o a un descrittore di sicurezza esistente, **CreatePrivateObjectSecurity** crea un descrittore di sicurezza esclusivamente dalle informazioni nei descrittori di sicurezza esistenti.

La funzione [**LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) ottiene le informazioni sul descrittore di sicurezza da un [*descrittore di sicurezza autonomo*](/windows/desktop/SecGloss/s-gly)esistente. Queste informazioni includono la specifica del proprietario e del gruppo, il numero di voci ACE nell'elenco SACL o DACL e l'elenco di voci ACE nel SACL o nel DACL.

 

 

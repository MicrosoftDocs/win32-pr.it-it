---
description: Per creare un descrittore di sicurezza, un server protetto può utilizzare la stessa procedura utilizzata da un'applicazione per creare un descrittore di sicurezza per un oggetto a protezione diretta.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descrittori di sicurezza per oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bae6615f309e572dc2e22f76310ccdf84bbbf5fff504aef0331d7d8e6b60ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413731"
---
# <a name="security-descriptors-for-private-objects"></a>Descrittori di sicurezza per oggetti privati

Per creare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly), un server protetto può utilizzare la stessa procedura utilizzata da un'applicazione per creare un descrittore di sicurezza per un oggetto a protezione diretta. Per il codice di esempio, [vedere Creazione di un descrittore di sicurezza per un nuovo oggetto in C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md) In alternativa, un'applicazione server protetta può chiamare la [**funzione BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) per eseguire questa operazione. Se a **BuildSecurityDescriptor** viene fornito un puntatore a un descrittore di sicurezza auto-relativo esistente, il nuovo descrittore di sicurezza verrà compilato con le informazioni derivate da tale descrittore di sicurezza unite con le nuove informazioni di controllo di accesso passate come parametri nella chiamata di funzione. [](/windows/desktop/SecGloss/s-gly) Il proprietario e il gruppo vengono specificati facoltativamente dalle strutture [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) passate alla funzione. Il descrittore di sicurezza creato da **BuildSecurityDescriptor** è in *formato auto-relativo.*

Inoltre, l'API Windows fornisce un set di funzioni per unire le informazioni di sicurezza client con le informazioni ereditate dal descrittore di sicurezza per un oggetto padre o da un descrittore di sicurezza predefinito. Le funzioni [**CreatePrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) [**GetPrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity) [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity) [**e DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) consentono di recuperare informazioni predefinite da un [*token*](/windows/desktop/SecGloss/a-gly)di accesso, supportare l'ereditarietà e modificare parti specifiche del descrittore di sicurezza. Ciò può essere utile quando un client crea un oggetto privato in una gerarchia di oggetti protetti. Ad esempio, è possibile usare la funzione **CreatePrivateObjectSecurity** per creare un descrittore di sicurezza che contiene le voci ACE specificate dal client, le voci ACE ereditate da un oggetto padre e il proprietario predefinito dal token di accesso del client che crea. Mentre [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crea descrittori di sicurezza dalle informazioni di controllo di accesso passate nella chiamata di funzione o da un descrittore di sicurezza esistente, **CreatePrivateObjectSecurity** crea un descrittore di sicurezza esclusivamente dalle informazioni nei descrittori di sicurezza esistenti.

[**La funzione LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) ottiene informazioni sul descrittore di sicurezza da un [*descrittore di sicurezza auto-relativo esistente.*](/windows/desktop/SecGloss/s-gly) Queste informazioni includono la specifica del proprietario e del gruppo, il numero di voci ACE nell'elenco SACL o DACL e l'elenco di ACE nell'elenco SACL o DACL.

 

 

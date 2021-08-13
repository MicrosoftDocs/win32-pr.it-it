---
description: Ogni SID (User and Group Security Identifier) in un token di accesso ha un set di attributi che controllano il modo in cui il sistema usa il SID in un controllo di accesso. Nella tabella seguente sono elencati gli attributi che controllano il controllo di accesso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Attributi SID in un token di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413421"
---
# <a name="sid-attributes-in-an-access-token"></a>Attributi SID in un token di accesso

Ogni SID (User and Group [*Security Identifier)*](/windows/desktop/SecGloss/s-gly) in un [*token*](/windows/desktop/SecGloss/a-gly) di accesso ha un set di attributi che controllano il modo in cui il sistema usa il SID in un controllo di accesso. Nella tabella seguente sono elencati gli attributi che controllano il controllo di accesso.



| Attributo                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_edizione Standard GRUPPO \_ ABILITATO              | Un SID con questo attributo è abilitato per i controlli di accesso. Quando il sistema esegue un controllo di accesso, verifica [](/windows/desktop/SecGloss/a-gly) le voci di controllo di accesso (ACE) consentite e negate di accesso che si applicano a uno dei SID abilitati nel token di accesso. Un SID senza questo attributo viene ignorato durante un controllo di accesso, a meno \_ edizione Standard'attributo GROUP \_ USE FOR DENY ONLY non sia \_ \_ \_ impostato.<br/> |
| \_edizione Standard UTILIZZO \_ DEL GRUPPO SOLO PER \_ \_ DENY \_ | Un SID con questo attributo è un SID di sola negazione. Quando il sistema esegue un controllo di accesso, verifica la presenza di ACE negate di accesso che si applicano al SID, ma ignora le ACE consentite per l'accesso per il SID. Se questo attributo è impostato, l'edizione Standard GROUP ENABLED non è impostato e il \_ \_ SID non può essere rienabled.<br/>                                                                                                                                                          |



 

Per impostare o cancellare \_ l edizione Standard'attributo GROUP ENABLED di un SID di \_ gruppo, usare la [**funzione AdjustTokenGroups.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) Non è possibile disabilitare un SID di gruppo con l'edizione Standard \_ GROUP \_ MANDATORY. Non è possibile **usare AdjustTokenGroups** per disabilitare il SID utente di un token di accesso.

Per determinare se un SID è abilitato in un token, ad esempio se ha l'attributo EDIZIONE STANDARD GROUP ENABLED, chiamare la \_ \_ funzione [**CheckTokenMembership.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)

Per impostare l'attributo EDIZIONE STANDARD GROUP USE FOR DENY ONLY di un SID, includere il SID nell'elenco dei SID di sola negazione specificati quando si chiama la \_ \_ funzione \_ \_ \_ [**CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) **CreateRestrictedToken** può applicare l'attributo edizione Standard GROUP USE FOR DENY ONLY a qualsiasi SID, inclusi il SID utente e i SID del gruppo con \_ \_ l'attributo EDIZIONE STANDARD GROUP \_ \_ \_ \_ \_ MANDATORY. Tuttavia, non è possibile rimuovere l'attributo di sola negazione da un SID, né usare [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) per impostare l'attributo edizione Standard GROUP ENABLED su un SID di sola \_ \_ negazione.

Per ottenere gli attributi di un SID, chiamare la [**funzione GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con il valore TokenGroups. La funzione restituisce una matrice di [**strutture SID \_ E \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) che identificano i SID del gruppo e i relativi attributi.

 


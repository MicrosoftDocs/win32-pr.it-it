---
description: Ogni ID di sicurezza (SID) di utenti e gruppi in un token di accesso dispone di un set di attributi che controllano il modo in cui il sistema usa il SID in un controllo di accesso. Nella tabella seguente sono elencati gli attributi che controllano il controllo dell'accesso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Attributi SID in un token di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a93e180c8c6ffe03a26591d5b9f722c2266356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752743"
---
# <a name="sid-attributes-in-an-access-token"></a>Attributi SID in un token di accesso

Ogni [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) di utenti e gruppi in un [*token di accesso*](/windows/desktop/SecGloss/a-gly) dispone di un set di attributi che controllano il modo in cui il sistema usa il SID in un controllo di accesso. Nella tabella seguente sono elencati gli attributi che controllano il controllo dell'accesso.



| Attributo                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_gruppo se \_ abilitato              | Un SID con questo attributo è abilitato per i controlli di accesso. Quando il sistema esegue un controllo di accesso, verifica la presenza di [*voci di controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACE) consentite e di accesso negato che si applicano a uno dei SID abilitati nel token di accesso. Un SID senza questo attributo viene ignorato durante un controllo di accesso, a meno che non \_ sia impostato il gruppo se non \_ si utilizza l' \_ \_ \_ attributo Deny only.<br/> |
| \_ \_ uso del gruppo \_ se \_ solo per Deny \_ | Un SID con questo attributo è un SID di sola negazione. Quando il sistema esegue un controllo di accesso, verifica se sono presenti Ace negate per l'accesso che si applicano al SID, ma ignora le voci ACE consentite per l'accesso al SID. Se questo attributo è impostato, l' \_ attributo gruppo se \_ abilitato non è impostato e non è possibile riabilitare il SID.<br/>                                                                                                                                                          |



 

Per impostare o deselezionare l' \_ attributo se Group \_ Enabled di un SID di gruppo, usare la funzione [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) . Non è possibile disabilitare un SID di gruppo con l' \_ attributo se Group \_ obbligatorio. Non è possibile usare **AdjustTokenGroups** per disabilitare il SID utente di un token di accesso.

Per determinare se un SID è abilitato in un token, ovvero se ha l' \_ attributo if Group \_ Enabled, chiamare la funzione [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) .

Per impostare il \_ gruppo se \_ usare \_ l' \_ \_ attributo Deny only di un SID, includere il SID nell'elenco dei SID di sola negazione specificati quando si chiama la funzione [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . **CreateRestrictedToken** può applicare il \_ gruppo se \_ per \_ l' \_ \_ attributo Deny only a qualsiasi SID, inclusi il SID utente e i SID di gruppo che hanno l' \_ \_ attributo obbligatorio se Group. Tuttavia, non è possibile rimuovere l'attributo di sola negazione da un SID, né usare [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) per impostare l'attributo se \_ Group \_ Enabled su un SID di sola negazione.

Per ottenere gli attributi di un SID, chiamare la funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con il valore tokenGroups. La funzione restituisce una matrice di strutture [**SID \_ e \_ Attributes**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) che identificano i SID di gruppo e i relativi attributi.

 


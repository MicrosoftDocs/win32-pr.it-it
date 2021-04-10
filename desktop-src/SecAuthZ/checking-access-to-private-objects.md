---
description: Un'applicazione server protetta deve verificare i diritti di accesso dei client prima di consentire al client di accedere a un oggetto privato protetto.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Controllo dell'accesso agli oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966762"
---
# <a name="checking-access-to-private-objects"></a>Controllo dell'accesso agli oggetti privati

Un'applicazione server protetta deve verificare i diritti di accesso di un client prima di consentire al client di accedere a un oggetto privato protetto. A tale scopo, il server passa un [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly), un descrittore di sicurezza e un set di diritti di accesso richiesti a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). Le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nel DACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificano i diritti di accesso consentiti o negati a diversi trustee. La funzione **AccessCheck** confronta il trustee in ogni voce ACE con i trustee identificati nel token di rappresentazione. Per una descrizione dell'algoritmo utilizzato per concedere o negare l'accesso, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

La funzione [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) esegue un controllo di accesso simile. Inoltre, genera i record di controllo nel registro eventi di sicurezza a seconda del SACL nel descrittore di sicurezza.

Le funzioni [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) e [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) sono simili a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , tranne per il fatto che consentono di controllare l'accesso agli oggetti sottooggetti di un oggetto, ad esempio set di proprietà o proprietà. Le funzioni [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) e [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) sono simili anche a **AccessCheck** , ad eccezione del fatto che forniscono i risultati del controllo dell'accesso per ogni sottooggetto in una gerarchia delle proprietà e dei set di proprietà dell'oggetto. Queste funzioni usano la struttura dell' [**\_ \_ elenco dei tipi di oggetto**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) per descrivere la gerarchia di oggetti per cui viene controllato l'accesso. Le funzioni che generano un messaggio di controllo usano il tipo di enumerazione [**Audit \_ Event \_ Type**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) per indicare se l'oggetto sottoposto a verifica è un oggetto del servizio directory. Per ulteriori informazioni sulla gerarchia di un oggetto e dei relativi oggetti SubObject, vedere [ACE per controllare l'accesso alle proprietà di un oggetto](aces-to-control-access-to-an-object-s-properties.md).

I diritti di accesso richiesti passati alle funzioni [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) non devono includere [diritti di accesso generici](generic-access-rights.md). Il server può utilizzare la funzione [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) per convertire i diritti di accesso generici nei diritti specifici e standard corrispondenti in base al mapping specificato nella struttura di [**\_ mapping generica**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

Le funzioni [**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) e [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) confrontano una [*maschera di accesso*](/windows/desktop/SecGloss/a-gly) richiesta con una maschera di accesso concessa.

Per il codice di esempio che usa la funzione [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , vedere [Verifica dell'accesso client con ACL in C++](verifying-client-access-with-acls-in-c--.md).

La funzione [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) crea e restituisce un descrittore di sicurezza in un formato che consente la propagazione automatica di ACE ereditabili. Questo descrittore di sicurezza contiene tutte le voci ACE, ereditate e non ereditate, nel descrittore di sicurezza corrente ed è in formato [*relativo*](/windows/desktop/SecGloss/s-gly) . La funzione **ConvertToAutoInheritPrivateObjectSecurity** determina se le voci ACE vengono ereditate o non ereditate confrontando tutte le voci ACE nel descrittore di sicurezza corrente con tutte le voci ACE nel descrittore di sicurezza padre. Potrebbe non essere presente una corrispondenza uno-a-uno tra i due gruppi di voci ACE. Ad esempio, una voce ACE che consente l'autorizzazione di lettura/scrittura può essere equivalente a due ACE: una voce ACE che consente l'autorizzazione di lettura e una voce ACE che consente l'autorizzazione di scrittura. Non è possibile specificare un descrittore di sicurezza padre quando il descrittore di sicurezza corrente è l'elemento padre.

 

 

---
description: Un'applicazione server protetta deve controllare i diritti di accesso di un client prima di consentire al client di accedere a un oggetto privato protetto.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Controllo dell'accesso agli oggetti privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f31f8ed05c16eed09cdd45da78f8fe58ecf41e283f6e6c37e7bc0480e63422d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783175"
---
# <a name="checking-access-to-private-objects"></a>Controllo dell'accesso agli oggetti privati

Un'applicazione server protetta deve controllare i diritti di accesso di un client prima di consentire al client di accedere a un oggetto privato protetto. A tale scopo, il server passa un [*token*](/windows/desktop/SecGloss/i-gly)di rappresentazione, un descrittore di sicurezza e un set di diritti di accesso richiesti a [**AccessCheck.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) Le [*voci di controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACE) [*nell'elenco*](/windows/desktop/SecGloss/s-gly) DACL del descrittore di sicurezza specificano i diritti di accesso consentiti o negati a vari fiduciari. La **funzione AccessCheck** confronta il trustee in ogni ACE con i fiduciari identificati nel token di rappresentazione. Per una descrizione dell'algoritmo usato per concedere o negare l'accesso, vedere [Come gli daCL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

La [**funzione AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) esegue un controllo di accesso simile. Genera inoltre record di controllo nel registro eventi di sicurezza a seconda dell'elenco sacl nel descrittore di sicurezza.

Le funzioni [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) e [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) sono simili a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) ad eccezione del fatto che consentono di controllare l'accesso ai sottooggetti di un oggetto, ad esempio set di proprietà o proprietà. Anche le funzioni [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) e [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) sono simili a **AccessCheck,** con la differenza che forniscono i risultati del controllo di accesso per ogni sottooggetto in una gerarchia delle proprietà e dei set di proprietà dell'oggetto. Queste funzioni usano la [**struttura OBJECT \_ TYPE \_ LIST**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) per descrivere la gerarchia di oggetti per cui viene controllato l'accesso. Le funzioni che generano un messaggio di controllo usano il tipo di enumerazione [**AUDIT \_ EVENT \_ TYPE**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) per indicare se l'oggetto controllato è un oggetto del servizio directory. Per altre informazioni sulla gerarchia di un oggetto e dei relativi sottooggetti, vedere [ACE to Control Access to an Object's Properties (ACE per controllare l'accesso](aces-to-control-access-to-an-object-s-properties.md)alle proprietà di un oggetto).

I diritti di accesso richiesti passati alle [**funzioni AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) e [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) non devono includere diritti [di accesso generici.](generic-access-rights.md) Il server può usare la [**funzione MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) per convertire tutti i diritti di accesso generici nei diritti di accesso specifici e standard corrispondenti in base al mapping specificato nella struttura [**GENERIC \_ MAPPING.**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)

Le [**funzioni AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) e [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) confrontano una maschera di accesso richiesta con una maschera di accesso concessa. [](/windows/desktop/SecGloss/a-gly)

Per codice di esempio che usa la [**funzione AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) vedere Verifica dell'accesso client con [gli ACL in C++.](verifying-client-access-with-acls-in-c--.md)

La [**funzione ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) crea e restituisce un descrittore di sicurezza in un formato che consente la propagazione automatica delle voci ACE ereditabili. Questo descrittore di sicurezza contiene tutte le voci ACE, ereditate e non ereditate, nel descrittore di sicurezza corrente ed è in [*formato self-relative.*](/windows/desktop/SecGloss/s-gly) La funzione **ConvertToAutoInheritPrivateObjectSecurity** determina se le voci ACE vengono ereditate o non ereditate confrontando tutte le voci ACE nel descrittore di sicurezza corrente con tutte le voci ACE nel descrittore di sicurezza padre. Potrebbe non esserci una corrispondenza uno-a-uno tra i due gruppi di ACE. Ad esempio, una ACE che consente l'autorizzazione di lettura/scrittura può essere equivalente a due voci ACE: una ACE che consente l'autorizzazione di lettura e una ACE che consente l'autorizzazione di scrittura. Un descrittore di sicurezza padre non può essere fornito quando il descrittore di sicurezza corrente è l'elemento padre.

 

 

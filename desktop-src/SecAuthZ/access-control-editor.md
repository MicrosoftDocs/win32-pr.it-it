---
description: Set di finestre delle proprietà e pagine delle proprietà che consentono all'utente di visualizzare e modificare i componenti di un descrittore di sicurezza degli oggetti.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Editor di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ed7c210c747278d35537fc010c66b60f0057d9a61b407eb04e993f8928f2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914679"
---
# <a name="access-control-editor"></a>Editor di controllo di accesso

L'editor del controllo di accesso è un set di finestre delle proprietà e pagine delle proprietà che consentono all'utente di visualizzare e modificare i componenti del descrittore di sicurezza [*di un oggetto*](/windows/desktop/SecGloss/s-gly). L'editor è costituito da due parti principali:

-   Pagina [delle proprietà di sicurezza](basic-security-property-page.md) di base che fornisce una semplice interfaccia per la modifica delle voci di controllo di accesso (ACE) nell'elenco di controllo di accesso discrezionale (DACL) di un oggetto. [](/windows/desktop/SecGloss/a-gly) [](/windows/desktop/SecGloss/d-gly) Questa pagina può includere un **pulsante** Avanzate facoltativo che visualizza la finestra delle proprietà sicurezza avanzata.
-   Una [](advanced-security-property-sheet.md) finestra delle proprietà di sicurezza avanzata con pagine delle proprietà che consentono all'utente di modificare l'elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL) dell'oggetto, modificare il proprietario dell'oggetto o eseguire la modifica avanzata dell'elenco DACL dell'oggetto.

La [**funzione CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crea la pagina delle proprietà di sicurezza di base. È quindi possibile usare la [**funzione PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) o il [**messaggio \_ PSM ADDPAGE**](../controls/psm-addpage.md) per aggiungere questa pagina a una finestra delle proprietà.

In alternativa, è possibile usare la [**funzione EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) per visualizzare una finestra delle proprietà contenente la pagina delle proprietà di sicurezza di base.

Sia per [**CreateSecurityPage che**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) [**per EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), il chiamante deve passare un puntatore a un'implementazione [**dell'interfaccia ISecurityInformation.**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) L'editor di controllo di accesso chiama i metodi di questa interfaccia per recuperare le informazioni di controllo di accesso sull'oggetto modificato e per passare l'input dell'utente all'applicazione. I **metodi ISecurityInformation** hanno gli scopi seguenti:

-   Per inizializzare le pagine delle proprietà.

    L'implementazione [**del metodo GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) passa una [**struttura SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) all'editor. Questa struttura specifica le pagine delle proprietà che si desidera visualizzare nell'editor e altre informazioni che determinano le opzioni di modifica disponibili per l'utente.

-   Per fornire informazioni di sicurezza sull'oggetto in corso di modifica.

    [**L'implementazione GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) passa il descrittore di [*sicurezza iniziale*](/windows/desktop/SecGloss/s-gly) dell'oggetto all'editor. I [**metodi GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) e [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) forniscono informazioni sui diritti di accesso dell'oggetto. Il [**metodo GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) fornisce informazioni su come le ACE dell'oggetto possono essere ereditate dagli oggetti figlio.

-   Per passare l'input dell'utente all'applicazione.

    Quando l'utente fa clic su **Ok** o **Applica,** l'editor chiama il [**metodo SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) per passare un descrittore di sicurezza contenente le modifiche dell'utente.

 

 

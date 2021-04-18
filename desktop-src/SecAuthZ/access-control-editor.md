---
description: Set di finestre delle proprietà e pagine delle proprietà che consentono all'utente di visualizzare e modificare i componenti di un descrittore di sicurezza degli oggetti.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Editor di controllo di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313723"
---
# <a name="access-control-editor"></a>Editor di controllo di accesso

L'editor di controllo di accesso è un set di finestre delle proprietà e pagine delle proprietà che consentono all'utente di visualizzare e modificare i componenti del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto. L'editor è costituito da due parti principali:

-   [Pagina delle proprietà di sicurezza di base](basic-security-property-page.md) che fornisce un'interfaccia semplice per la modifica delle voci di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di [*controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) di un oggetto. Questa pagina può includere un pulsante **avanzato** facoltativo che visualizza la finestra delle proprietà sicurezza avanzata.
-   Una [finestra delle proprietà di sicurezza avanzata](advanced-security-property-sheet.md) con le pagine delle proprietà che consentono all'utente di modificare l' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) dell'oggetto, modificare il proprietario dell'oggetto o eseguire una modifica avanzata dell'elenco DACL dell'oggetto.

La funzione [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crea la pagina delle proprietà di sicurezza di base. È quindi possibile usare la funzione [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) o il [**messaggio \_ ADDPAGE di PSM**](../controls/psm-addpage.md) per aggiungere questa pagina a una finestra delle proprietà.

In alternativa, è possibile usare la funzione [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) per visualizzare una finestra delle proprietà che contiene la pagina delle proprietà sicurezza di base.

Per [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) e [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), il chiamante deve passare un puntatore a un'implementazione dell'interfaccia [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) . L'editor di controllo di accesso chiama i metodi di questa interfaccia per recuperare le informazioni di controllo di accesso sull'oggetto modificato e per passare di nuovo l'input dell'utente all'applicazione. I metodi **ISecurityInformation** hanno gli scopi seguenti:

-   Per inizializzare le pagine delle proprietà.

    L'implementazione del metodo [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) passa una struttura [**di \_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) all'editor. Questa struttura specifica le pagine delle proprietà che si desidera visualizzare nell'editor e altre informazioni che determinano le opzioni di modifica disponibili per l'utente.

-   Per fornire informazioni sulla sicurezza relative all'oggetto da modificare.

    L'implementazione [**GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) passa il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) iniziale dell'oggetto all'editor. I metodi [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) e [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) forniscono informazioni sui diritti di accesso dell'oggetto. Il metodo [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) fornisce informazioni sul modo in cui le voci ACE dell'oggetto possono essere ereditate dagli oggetti figlio.

-   Per passare di nuovo l'input dell'utente all'applicazione.

    Quando l'utente fa clic su **OK** o **applica**, l'editor chiama il metodo di [**sicurezza**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) per passare un descrittore di sicurezza contenente le modifiche dell'utente.

 

 

---
description: Pagina iniziale della finestra delle proprietà visualizzata dalla funzione EditSecurity. È anche possibile usare la funzione CreateSecurityPage per creare una pagina delle proprietà di sicurezza di base da inserire nella finestra delle proprietà.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Pagina delle proprietà sicurezza di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f839058d8cd9c9a4c9d1a20dab96620d1e731d23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130422"
---
# <a name="basic-security-property-page"></a>Pagina delle proprietà sicurezza di base

La pagina delle proprietà sicurezza di base è la pagina iniziale della finestra delle proprietà visualizzata dalla funzione [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) . È anche possibile usare la funzione [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) per creare una pagina delle proprietà di sicurezza di base da inserire nella finestra delle proprietà.

Nella pagina delle proprietà viene visualizzato un elenco dei [trustee](trustees.md) denominati nelle [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (DACL) dell'elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto. La pagina contiene anche un elenco dei diritti di accesso supportati dall'oggetto. Quando l'utente seleziona un nome dall'elenco dei trustee, le caselle di controllo accanto a ogni diritto di accesso indicano i diritti consentiti o negati per tale trustee. L'utente può quindi selezionare o deselezionare le caselle di controllo per modificare i diritti di accesso del trustee. L'utente può anche aggiungere o rimuovere i trustee dall'elenco.

La pagina delle proprietà sicurezza di base non può visualizzare voci ACE complesse, ad esempio [ACE specifiche dell'oggetto](object-specific-aces.md)o informazioni sull'ereditarietà ACE. Per consentire all'utente di visualizzare o modificare tali informazioni, è possibile includere un pulsante **Avanzate** nella pagina sicurezza di base. L'utente può fare clic sul pulsante **Avanzate** per visualizzare una [finestra delle proprietà di sicurezza avanzata](advanced-security-property-sheet.md). In questa finestra delle proprietà sono presenti pagine delle proprietà che consentono all'utente di modificare l' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL) dell'oggetto, modificare il proprietario dell'oggetto o eseguire una modifica avanzata del DACL dell'oggetto. Per visualizzare il pulsante **Avanzate** , impostare il \_ flag si Advanced nella struttura di [**\_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituito dall'implementazione di [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

È possibile usare il membro **pszPageTitle** della struttura [**di \_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) per specificare il titolo della pagina delle proprietà di sicurezza di base. Il titolo predefinito è **sicurezza**.

 

 

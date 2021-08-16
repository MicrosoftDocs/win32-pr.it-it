---
description: Pagina iniziale della finestra delle proprietà visualizzata dalla funzione EditSecurity. È anche possibile usare la funzione CreateSecurityPage per creare una pagina delle proprietà di sicurezza di base da inserire nella finestra delle proprietà.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Pagina delle proprietà Sicurezza di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783708"
---
# <a name="basic-security-property-page"></a>Pagina delle proprietà Sicurezza di base

La pagina delle proprietà di sicurezza di base è la pagina iniziale della finestra delle proprietà visualizzata dalla [**funzione EditSecurity.**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) È anche possibile usare la [**funzione CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) per creare una pagina delle proprietà di sicurezza di base da inserire nella finestra delle proprietà.

Nella pagina delle proprietà viene visualizzato un elenco dei [trustee](trustees.md) denominati nelle voci di controllo di accesso [](/windows/desktop/SecGloss/a-gly) (ACE) dell'elenco di controllo di accesso discrezionale [](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto. La pagina contiene anche un elenco dei diritti di accesso supportati dall'oggetto . Quando l'utente seleziona un nome dall'elenco dei fiduciari, le caselle di controllo accanto a ogni diritto di accesso indicano i diritti consentiti o negati per tale trustee. L'utente può quindi selezionare o deselezionare le caselle di controllo per modificare i diritti di accesso del trustee. L'utente può anche aggiungere o rimuovere i trustee dall'elenco.

Nella pagina delle proprietà di sicurezza di base non è possibile visualizzare ACE complesse, ad esempio ACE specifiche dell'oggetto [o](object-specific-aces.md)informazioni sull'ereditarietà ACE. Per consentire all'utente di visualizzare o modificare tali informazioni, è possibile includere un **pulsante** Avanzate nella pagina sicurezza di base. L'utente può fare clic **sul pulsante** Avanzate per visualizzare una finestra delle proprietà di [sicurezza avanzata.](advanced-security-property-sheet.md) Questa finestra delle proprietà include pagine delle proprietà [](/windows/desktop/SecGloss/s-gly) che consentono all'utente di modificare l'elenco di controllo di accesso di sistema (SACL) dell'oggetto, modificare il proprietario dell'oggetto o eseguire la modifica avanzata dell'elenco DACL dell'oggetto. Per visualizzare il **pulsante Avanzate,** impostare il flag SI ADVANCED nella struttura SI OBJECT INFO restituita dall'implementazione \_ di [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

È possibile usare il **membro pszPageTitle** della struttura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) per specificare il titolo della pagina delle proprietà di sicurezza di base. Il titolo predefinito è **Sicurezza**.

 

 

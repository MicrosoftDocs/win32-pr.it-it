---
description: L'editor di controllo di accesso può includere una pagina delle proprietà Controllo che consente all'utente di visualizzare e modificare le voci di controllo di accesso (ACE) in un elenco di controllo di accesso di sistema (SACL) di oggetti. Per altre informazioni sugli elenchi di controllo di accesso (ACL), vedere Elenchi di controllo di accesso (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Pagina delle proprietà Controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf116a9079c5b7b6dfeb7e6df57b45d6a0a2555c14de88a32fee4fadcdc6373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784319"
---
# <a name="auditing-property-page"></a>Pagina delle proprietà Controllo

L'editor di controllo  di accesso può includere una pagina delle proprietà Controllo che consente all'utente di visualizzare e modificare le voci di controllo di accesso [](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di controllo di accesso [*di*](/windows/desktop/SecGloss/s-gly) sistema (SACL) di un oggetto. Per altre informazioni sugli elenchi di controllo di accesso (ACL), vedere [Elenchi di controllo](access-control-lists.md) di accesso (ACL).

**Per visualizzare la pagina delle proprietà Controllo**

-   Nella pagina [delle proprietà sicurezza di base fare](basic-security-property-page.md)clic su **Avanzate.** La **pagina delle proprietà** Controllo si trova nella finestra delle proprietà Sicurezza [avanzata](advanced-security-property-sheet.md).

Per includere la **pagina** delle proprietà Controllo, impostare i flag **SI \_ ADVANCED** e **SI EDIT \_ \_ AUDITS** nella struttura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituita dall'implementazione [**di ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)

 

 

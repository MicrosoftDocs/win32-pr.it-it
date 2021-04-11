---
description: L'editor di controllo di accesso può includere una pagina delle proprietà di controllo che consente all'utente di visualizzare e modificare le voci di controllo di accesso (ACE) in un elenco di controllo di accesso di sistema (SACL) degli oggetti. Per ulteriori informazioni sui SACL, vedere elenchi di controllo di accesso (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Pagina delle proprietà controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232423"
---
# <a name="auditing-property-page"></a>Pagina delle proprietà controllo

L'editor di controllo di accesso può includere una pagina **delle proprietà di controllo che** consente all'utente di visualizzare e modificare le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL) di un oggetto. Per ulteriori informazioni sui SACL, vedere [elenchi di controllo di accesso](access-control-lists.md) (ACL).

**Per visualizzare la pagina delle proprietà del controllo**

-   Nella [pagina delle proprietà sicurezza di base](basic-security-property-page.md)fare clic su **Avanzate**. La pagina delle proprietà **controllo** si trova nella [finestra delle proprietà sicurezza avanzata](advanced-security-property-sheet.md).

Per includere la pagina delle proprietà di controllo, impostare i flag per **la \_ modifica \_** di **si \_ avanzata** e la modifica del **controllo** di stato nella struttura di [**\_ \_ informazioni sull'oggetto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) restituita dall'implementazione di [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 

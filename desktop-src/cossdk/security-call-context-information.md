---
description: Informazioni sul contesto di chiamata di sicurezza
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informazioni sul contesto di chiamata di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aed07f79fdba16f0ea6139a58cc50871d795e1eacbf94737b04dbf5f1fe900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546868"
---
# <a name="security-call-context-information"></a>Informazioni sul contesto di chiamata di sicurezza

La sicurezza basata sui ruoli si basa su un meccanismo generale che consente di recuperare informazioni sulla sicurezza relative a tutti i chiamanti upstream nella catena di chiamate al componente. Queste informazioni sono disponibili solo quando è abilitato il controllo dei ruoli a livello di componente. Per informazioni dettagliate su come impostare la sicurezza a livello di componente, vedere [Impostazione di un livello di sicurezza per i controlli di accesso.](setting-a-security-level-for-access-checks.md)

È possibile usare [**l'interfaccia ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) per accedere alle informazioni sul contesto di chiamata di sicurezza a livello di codice. Per una descrizione, vedere [Sicurezza dei componenti a livello di codice.](programmatic-component-security.md)

Il contesto di chiamata di sicurezza viene passato ogni volta che viene superato un limite di sicurezza. Per le chiamate tra componenti all'interno di un'applicazione, che si trovano all'interno dello stesso limite di sicurezza, non viene passata alcuna informazione sul contesto di chiamata. Per le chiamate tra processi o tra applicazioni all'interno di un processo, le informazioni sul contesto di chiamata passano lungo.

Questa funzionalità è particolarmente utile se si desidera eseguire operazioni di controllo e registrazione dettagliate. È possibile recuperare e registrare le informazioni di sicurezza per ogni chiamante upstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Uso dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




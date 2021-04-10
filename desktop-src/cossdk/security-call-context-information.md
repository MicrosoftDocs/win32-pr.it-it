---
description: Informazioni sul contesto delle chiamate di sicurezza
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informazioni sul contesto delle chiamate di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213e21d684d004ed18e5b9aa536e03ae8292307e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225775"
---
# <a name="security-call-context-information"></a>Informazioni sul contesto delle chiamate di sicurezza

La protezione basata sui ruoli si basa su un meccanismo generale che consente di recuperare le informazioni di sicurezza relative a tutti i chiamanti upstream nella catena di chiamate al componente. Queste informazioni sono disponibili solo quando è abilitato il controllo del ruolo a livello di componente. Per informazioni dettagliate su come impostare la sicurezza a livello di componente, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).

È possibile usare l'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) per accedere alle informazioni di contesto delle chiamate di sicurezza a livello di codice. Per una descrizione, vedere [sicurezza dei componenti programmatici](programmatic-component-security.md).

Il contesto della chiamata di sicurezza viene passato ogni volta che viene superato un limite di sicurezza. Per le chiamate tra i componenti all'interno di un'applicazione, che si trovano all'interno dello stesso limite di sicurezza, non vengono passate informazioni sul contesto di chiamata. Per le chiamate tra i processi o tra le applicazioni all'interno di un processo, le informazioni sul contesto di chiamata scorrono lungo.

Questa funzionalità è particolarmente utile se si desidera eseguire operazioni di controllo e registrazione dettagliate. È possibile recuperare e registrare le informazioni di sicurezza per ogni chiamante upstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione efficace dei ruoli](designing-roles-effectively.md)
</dt> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Utilizzo dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




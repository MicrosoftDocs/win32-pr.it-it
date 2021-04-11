---
description: Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configurazione della sicurezza Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342141"
---
# <a name="configuring-role-based-security"></a>Configurazione della sicurezza Role-Based

Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività. Quando si progettano i componenti nell'applicazione, si definiscono i ruoli necessari per proteggere l'accesso a tali componenti. Si decidono inoltre i ruoli da assegnare ai componenti, alle interfacce e ai metodi dell'applicazione. Durante l'integrazione dell'applicazione, si utilizza lo strumento di amministrazione Servizi componenti per aggiungere i ruoli definiti all'applicazione e assegnare ogni ruolo ai componenti, alle interfacce e ai metodi appropriati.

Per la configurazione della sicurezza basata sui ruoli, seguire questa procedura:

1.  Abilitare i controlli di accesso a livello di applicazione. Per attivare il controllo di sicurezza per un'applicazione. Per informazioni dettagliate su come eseguire questo passaggio, vedere [Abilitazione dei controlli di accesso per un'applicazione](enabling-access-checks-for-an-application.md) .
2.  Imposta il livello di sicurezza per i controlli di accesso. Per impostare la sicurezza a livello di processo o di componente. Per informazioni dettagliate su come eseguire questo passaggio, vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md) .
3.  Abilitare i controlli di accesso a livello di componente. Per attivare il controllo di sicurezza a livello di componente, interfaccia e metodo. Per informazioni dettagliate su come eseguire questo passaggio, vedere [Abilitazione dei controlli di accesso a livello di componente](enabling-access-checks-at-the-component-level.md) .
4.  Definire i ruoli per un'applicazione. Per creare ruoli per un'applicazione. Per informazioni dettagliate su come eseguire questo passaggio, vedere [definizione dei ruoli per un'applicazione](defining-roles-for-an-application.md) .
5.  Assegnare ruoli a componenti, interfacce o metodi. Per assegnare ruoli a risorse specifiche all'interno di un'applicazione. Per informazioni dettagliate su come eseguire questo passaggio [, vedere Assegnazione di ruoli a componenti, interfacce o metodi](assigning-roles-to-components--interfaces--or-methods.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Impostazione di un livello di rappresentazione](setting-an-impersonation-level.md)
</dt> </dl>

 

 




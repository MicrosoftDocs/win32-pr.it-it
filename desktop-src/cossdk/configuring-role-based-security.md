---
description: Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configurazione della Role-Based sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba7df6b11bf44b53adaa9776435e43eabe3188fccb789a01d996f45331298dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859061"
---
# <a name="configuring-role-based-security"></a>Configurazione della Role-Based sicurezza

Se l'applicazione COM+ usa la sicurezza basata sui ruoli, è necessario completare diverse attività. Quando si progettano i componenti nell'applicazione, si definiscono i ruoli necessari per proteggere l'accesso a tali componenti. È anche possibile decidere quali ruoli assegnare ai componenti, alle interfacce e ai metodi dell'applicazione. Durante l'integrazione dell'applicazione, si usa lo strumento amministrativo Servizi componenti per aggiungere i ruoli definiti all'applicazione e assegnare ogni ruolo ai componenti, alle interfacce e ai metodi appropriati.

Nella configurazione della sicurezza basata sui ruoli seguire questa procedura:

1.  Abilitare i controlli di accesso a livello di applicazione. Per attivare il controllo di sicurezza per un'applicazione. Per [informazioni dettagliate su come eseguire questo](enabling-access-checks-for-an-application.md) passaggio, vedere abilitazione dei controlli di accesso per un'applicazione.
2.  Impostare il livello di sicurezza per i controlli di accesso. Per impostare la sicurezza a livello di processo o a livello di processo e componente. Per [informazioni dettagliate su come eseguire questo passaggio,](setting-a-security-level-for-access-checks.md) vedere Impostazione di un livello di sicurezza per i controlli di accesso.
3.  Abilitare i controlli di accesso a livello di componente. Per attivare il controllo di sicurezza a livello di componente, interfaccia e metodo. Per [informazioni dettagliate su come eseguire questo passaggio,](enabling-access-checks-at-the-component-level.md) vedere Abilitazione dei controlli di accesso a livello di componente.
4.  Definire i ruoli per un'applicazione. Per creare ruoli per un'applicazione. Per [informazioni dettagliate su come eseguire questo passaggio,](defining-roles-for-an-application.md) vedere Definizione dei ruoli per un'applicazione.
5.  Assegnare ruoli a componenti, interfacce o metodi. Per assegnare ruoli a risorse specifiche all'interno di un'applicazione. Per [informazioni dettagliate su come eseguire questo passaggio,](assigning-roles-to-components--interfaces--or-methods.md) vedere Assegnazione di ruoli a componenti, interfacce o metodi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dei criteri di restrizione software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Impostazione di un livello di rappresentazione](setting-an-impersonation-level.md)
</dt> </dl>

 

 




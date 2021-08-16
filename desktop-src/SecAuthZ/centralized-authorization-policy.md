---
description: Lo scenario Dynamic Access Control (DAC) consente l'amministrazione centralizzata del controllo di accesso per scenari file server aziendali.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Criteri di autorizzazione centralizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a07730bff997b545285b0d2845547a4d5deaffe78324e354e7eecbf879b763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783190"
---
# <a name="centralized-authorization-policy"></a>Criteri di autorizzazione centralizzati

Lo [scenario Dynamic Access Control (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) consente l'amministrazione centralizzata del controllo di accesso per gli file server aziendali. La maggior parte delle organizzazioni ha più aree in cui vuole controllare l'accesso.

Alcuni esempi:

-   Controllo dell'accesso alle informazioni riservate, in cui i file contrassegnati come sensibili avrebbero autorizzazioni specifiche
-   Controllo dell'accesso ai file contenenti informazioni personali.)
-   Limitazione dell'accesso ai documenti in base ai criteri di conservazione delle organizzazioni.

Vengono fornite diverse nuove astrazioni dei criteri di autorizzazione per consentire a un amministratore di definire questi criteri in modo centralizzato e semplificare il processo di definizione consentendo a ognuno di questi requisiti di accesso di essere definiti e gestiti separatamente, ma applicati come un unico criterio.

Due nuovi oggetti criteri [](central-authorization-policies.md) di Active Directory, un criterio di autorizzazione centrale (cap) e una regola dei criteri di autorizzazione centrale (capr) vengono introdotti in Windows 8 per definire e applicare criteri di autorizzazione centralizzati in base alle espressioni di attestazioni e attributi delle risorse. [](central-authorization-policy-rule.md) nell'uso di questi oggetti un amministratore definisce un capr come criteri di autorizzazione specifici che possono essere applicati alle risorse che hanno un determinato attributo o soddisfano una determinata condizione di applicabilità. ad esempio documenti etichettati come "impatto aziendale elevato". Le mante possono essere definite per ogni criterio di controllo di accesso desiderato in un'organizzazione che può essere espresso e le risorse a cui deve essere applicato possono essere identificate, in termini di espressioni dac di Windows 8. un limite è una raccolta di capr che possono essere applicati insieme alle risorse. Il diagramma seguente illustra le relazioni tra cap e cap e cap e i passaggi concettuali necessari per definire e applicare questi oggetti alle risorse file. ![relazione tra mantelle e tappi](images/cap.png)

 

 

---
description: Lo scenario controllo dinamico degli accessi (DAC) consente l'amministrazione centralizzata del controllo degli accessi per gli scenari Enterprise file server.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Criteri di autorizzazione centralizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968752"
---
# <a name="centralized-authorization-policy"></a>Criteri di autorizzazione centralizzati

Lo [scenario controllo dinamico degli accessi (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) consente l'amministrazione centralizzata del controllo degli accessi per gli scenari Enterprise file server. La maggior parte delle organizzazioni dispone di più aree in cui desiderano controllare l'accesso.

Alcuni esempi:

-   Controllo dell'accesso alle informazioni riservate, in cui i file contrassegnati come sensibili hanno autorizzazioni specifiche
-   Controllo dell'accesso ai file contenenti informazioni personali (PII)
-   Limitazione dell'accesso ai documenti in base ai criteri di conservazione delle organizzazioni.

Sono disponibili diverse nuove astrazioni dei criteri di autorizzazione che consentono a un amministratore di definire questi criteri in modo centralizzato e di semplificare il processo di definizione consentendo a ognuno di questi requisiti di accesso di essere definiti e gestiti separatamente, ma applicati come un criterio.

In Windows 8 sono stati introdotti due nuovi oggetti Criteri di Active Directory, un [criterio di autorizzazione centrale](central-authorization-policies.md) e una [regola dei criteri di autorizzazione centrale](central-authorization-policy-rule.md) (CAPR) per definire e applicare criteri di autorizzazione centralizzati basati su espressioni di attestazioni e attributi di risorse. Quando si usano questi oggetti, un amministratore definisce un Capr come criterio di autorizzazione specifico che può essere applicato a risorse che hanno un determinato attributo o che soddisfano una determinata condizione di applicabilità. ad esempio documenti con l'etichetta "High Business Impact". è possibile definire CAPES per ogni criterio di controllo di accesso desiderato in un'organizzazione che può essere espressa e le risorse a cui deve essere applicato possono essere identificate in termini di espressioni DAC di Windows 8. un limite è costituito da una raccolta di caprs che possono essere applicati insieme alle risorse. il diagramma seguente illustra le relazioni tra il CAP e il mantello e i passaggi concettuali necessari per la definizione e l'applicazione di questi oggetti alle risorse di file. ![relazione tra CAPES e Caps](images/cap.png)

 

 

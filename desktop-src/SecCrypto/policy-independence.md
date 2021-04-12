---
description: I certificati vengono concessi in base ai criteri che definiscono i criteri che i richiedenti devono soddisfare per ricevere un certificato.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Indipendenza dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346536"
---
# <a name="policy-independence"></a>Indipendenza dei criteri

I certificati vengono concessi in base ai criteri che definiscono i criteri che i richiedenti devono soddisfare per ricevere un certificato. Ad esempio, un criterio può essere quello di concedere i certificati commerciali solo se i candidati presentano l'identificazione di persona. Un altro criterio può concedere le [*credenziali*](../secgloss/c-gly.md) in base alle richieste di posta elettronica. Un'agenzia che rilascia carte di credito può scegliere di consultare un database e di effettuare richieste di telefonate prima di emettere una scheda.

I criteri sono implementati nei moduli dei criteri scritti in C++, C o Visual Basic. Le funzioni di Servizi certificati sono isolate dalle modifiche ai criteri che un'agenzia potrebbe implementare. Le modifiche ai criteri possono essere implementate completamente nel codice del modulo criteri del server. Un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) dell'organizzazione (Enterprise) deve usare solo il modulo criteri di organizzazione fornito da Microsoft.

 

 

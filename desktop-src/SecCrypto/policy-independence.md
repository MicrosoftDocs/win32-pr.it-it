---
description: I certificati vengono concessi in base ai criteri che definiscono i criteri che i richiedenti devono soddisfare per ricevere un certificato.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Indipendenza dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63afc249905dc03602e38458ba326674e033648669e3187d44e58a188b122d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978967"
---
# <a name="policy-independence"></a>Indipendenza dei criteri

I certificati vengono concessi in base ai criteri che definiscono i criteri che i richiedenti devono soddisfare per ricevere un certificato. Ad esempio, un criterio può essere quello di concedere certificati commerciali solo se i richiedenti presentano di persona la propria identificazione. Un altro criterio può concedere [*le credenziali in base*](../secgloss/c-gly.md) alle richieste di posta elettronica. Un'agenzia che emette carte di credito può scegliere di consultare un database ed effettuare richieste telefoniche prima di emettere una carta.

I criteri vengono implementati nei moduli dei criteri scritti in C++, C o Visual Basic. Le funzioni di Servizi certificati sono isolate da eventuali modifiche ai criteri che un'agenzia potrebbe implementare. Le modifiche ai criteri possono essere completamente implementate nel codice del modulo criteri server. [*Un'autorità di certificazione*](../secgloss/c-gly.md) dell'organizzazione (CA) deve usare solo il modulo Criteri aziendali fornito da Microsoft.

 

 

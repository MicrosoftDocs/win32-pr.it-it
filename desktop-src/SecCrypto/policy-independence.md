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
# <a name="policy-independence"></a><span data-ttu-id="3b771-103">Indipendenza dei criteri</span><span class="sxs-lookup"><span data-stu-id="3b771-103">Policy Independence</span></span>

<span data-ttu-id="3b771-104">I certificati vengono concessi in base ai criteri che definiscono i criteri che i richiedenti devono soddisfare per ricevere un certificato.</span><span class="sxs-lookup"><span data-stu-id="3b771-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="3b771-105">Ad esempio, un criterio può essere quello di concedere i certificati commerciali solo se i candidati presentano l'identificazione di persona.</span><span class="sxs-lookup"><span data-stu-id="3b771-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="3b771-106">Un altro criterio può concedere le [*credenziali*](../secgloss/c-gly.md) in base alle richieste di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3b771-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="3b771-107">Un'agenzia che rilascia carte di credito può scegliere di consultare un database e di effettuare richieste di telefonate prima di emettere una scheda.</span><span class="sxs-lookup"><span data-stu-id="3b771-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="3b771-108">I criteri sono implementati nei moduli dei criteri scritti in C++, C o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3b771-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="3b771-109">Le funzioni di Servizi certificati sono isolate dalle modifiche ai criteri che un'agenzia potrebbe implementare.</span><span class="sxs-lookup"><span data-stu-id="3b771-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="3b771-110">Le modifiche ai criteri possono essere implementate completamente nel codice del modulo criteri del server.</span><span class="sxs-lookup"><span data-stu-id="3b771-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="3b771-111">Un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) dell'organizzazione (Enterprise) deve usare solo il modulo criteri di organizzazione fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b771-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 

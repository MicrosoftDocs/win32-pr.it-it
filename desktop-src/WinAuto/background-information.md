---
title: Informazioni di base
description: Il componente Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano IAccessible per conto dei controlli Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116765"
---
# <a name="background-information"></a><span data-ttu-id="cc8f6-103">Informazioni di base</span><span class="sxs-lookup"><span data-stu-id="cc8f6-103">Background Information</span></span>

<span data-ttu-id="cc8f6-104">Il componente Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dei controlli Windows standard.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="cc8f6-105">Poiché questi proxy usano i messaggi Windows standard e le API specifiche del controllo per raccogliere informazioni su ogni controllo, non esiste alcun meccanismo diretto per la personalizzazione delle informazioni che questi proxy espongono tramite **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="cc8f6-106">Attualmente, è possibile personalizzare un'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente mediante tecniche di creazione di sottoclassi e wrapping.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="cc8f6-107">Tuttavia, queste tecniche sono noiose e soggette a errori.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="cc8f6-108">Infatti, la maggior parte del codice scritto per eseguire l'override di una o due proprietà riguarda l'implementazione della sottoclasse e del wrapping; solo una piccola frazione esegue la vera attività di override delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="cc8f6-109">L'annotazione dinamica migliora la situazione fornendo funzionalità simili senza richiedere la scrittura di codice per la creazione di sottoclassi o il ritorno a capo.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="cc8f6-110">È invece possibile concentrarsi sulla fornitura di codice che fornisca le informazioni corrette.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="cc8f6-111">L'annotazione dinamica consente agli sviluppatori di passare hint e altre informazioni utili a OLEACC per personalizzare le informazioni che espone.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="cc8f6-112">Questa funzionalità consente di ridurre il costo del supporto di Microsoft Active Accessibility e di consentire agli sviluppatori di migliorare notevolmente l'accessibilità delle interfacce utente.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 





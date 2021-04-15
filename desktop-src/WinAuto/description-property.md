---
title: Proprietà Description (funzionalità di accessibilità di Windows)
description: La proprietà Description di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474980"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="a9f27-103">Proprietà Description (funzionalità di accessibilità di Windows)</span><span class="sxs-lookup"><span data-stu-id="a9f27-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="a9f27-104">La proprietà **Description** viene spesso usata in modo non corretto e non è supportata dall'automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9f27-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="a9f27-105">Gli sviluppatori di Microsoft Active Accessibility server non devono utilizzare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9f27-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="a9f27-106">Se sono necessarie altre informazioni per gli scenari di accessibilità e automazione, usare le proprietà supportate dagli elementi di automazione interfaccia utente e dai pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9f27-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="a9f27-107">La proprietà **Description** di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9f27-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="a9f27-108">La descrizione viene utilizzata principalmente per fornire un contesto più ampio per utenti ipovedenti o ipovedenti, ma viene anche utilizzata per la ricerca del contesto o altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a9f27-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="a9f27-109">Questa proprietà può aiutare gli utenti a comprendere un'icona o l'aspetto visivo generale.</span><span class="sxs-lookup"><span data-stu-id="a9f27-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="a9f27-110">La proprietà **Description** viene recuperata chiamando [**IAccessible:: Get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span><span class="sxs-lookup"><span data-stu-id="a9f27-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="a9f27-111">Quando supportare la proprietà Description</span><span class="sxs-lookup"><span data-stu-id="a9f27-111">When to Support the Description Property</span></span>

<span data-ttu-id="a9f27-112">I server supportano la proprietà **Description** se la descrizione non è ovvia o se non è ridondante in base alle proprietà [**Name**](name-property.md), [**Role**](role-property.md), [**state**](state-property.md)e [**value**](value-property.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9f27-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="a9f27-113">Ad esempio, un pulsante con etichetta "OK" non richiede informazioni aggiuntive, mentre un pulsante che mostra un'immagine di un cactus.</span><span class="sxs-lookup"><span data-stu-id="a9f27-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="a9f27-114">Il **nome**, il **ruolo** e le proprietà della [**Guida**](help-property.md) per un pulsante di questo tipo ne descrivono lo scopo, ma la proprietà **Description** trasmette informazioni meno tangibili; ad esempio, "questo pulsante Mostra un'immagine di un cactus".</span><span class="sxs-lookup"><span data-stu-id="a9f27-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="a9f27-115">Un server Microsoft Active Accessibility può aggiungere il supporto per l'automazione dell'interfaccia utente usando un' [annotazione diretta](direct-annotation.md), usando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o implementando Microsoft Active Accessibility e l'automazione dell'interfaccia utente side-by-side con entrambe le implementazioni che gestiscono il messaggio [**WM \_ GetObject**](wm-getobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f27-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9f27-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9f27-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f27-117">Uso dell'annotazione diretta</span><span class="sxs-lookup"><span data-stu-id="a9f27-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="a9f27-118">Interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="a9f27-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 





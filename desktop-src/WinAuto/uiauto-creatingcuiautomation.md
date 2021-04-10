---
title: Creazione dell'oggetto CUIAutomation
description: Questa sezione descrive come iniziare a scrivere un'applicazione client di automazione interfaccia utente Microsoft creando un'istanza di un oggetto che implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- client, creazione oggetto CUIAutomation
- client, oggetto CUIAutomation
- Automazione interfaccia utente, oggetto CUIAutomation
- Automazione interfaccia utente, creazione oggetto CUIAutomation
- creazione dell'oggetto CUIAutomation
- Oggetto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963141"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="7997d-109">Creazione dell'oggetto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="7997d-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="7997d-110">Questa sezione descrive come iniziare a scrivere un'applicazione client di automazione interfaccia utente Microsoft creando un'istanza di un oggetto che implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="7997d-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="7997d-111">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7997d-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7997d-112">Oggetto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="7997d-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="7997d-113">Creazione dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="7997d-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="7997d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7997d-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="7997d-115">Oggetto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="7997d-115">The CUIAutomation Object</span></span>

<span data-ttu-id="7997d-116">Il primo passaggio nell'uso di automazione interfaccia utente consiste nel creare un oggetto della classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7997d-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="7997d-117">Questo oggetto espone l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , che rappresenta il gateway per tutti gli altri oggetti e le interfacce utilizzati dalle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="7997d-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="7997d-118">Tra le altre cose, **IUIAutomation** viene usato per le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="7997d-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="7997d-119">Sottoscrizione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="7997d-119">Subscribing to events.</span></span>
-   <span data-ttu-id="7997d-120">Creazione di condizioni.</span><span class="sxs-lookup"><span data-stu-id="7997d-120">Creating conditions.</span></span> <span data-ttu-id="7997d-121">Le condizioni sono oggetti utilizzati per limitare l'ambito delle ricerche degli elementi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7997d-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="7997d-122">Ottenere gli elementi di automazione interfaccia utente direttamente dal desktop (elemento radice) o dalle coordinate dello schermo o dagli handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="7997d-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="7997d-123">Creazione di oggetti Walker di albero che possono essere usati per spostarsi nella gerarchia degli elementi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7997d-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="7997d-124">Conversione di tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="7997d-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="7997d-125">Creazione dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="7997d-125">Creating the Object</span></span>

<span data-ttu-id="7997d-126">Per iniziare a usare automazione interfaccia utente nell'applicazione, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7997d-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="7997d-127">Includere UIAutomation. h nelle intestazioni del progetto.</span><span class="sxs-lookup"><span data-stu-id="7997d-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="7997d-128">UIAutomation. h riporta le altre intestazioni che definiscono l'API.</span><span class="sxs-lookup"><span data-stu-id="7997d-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="7997d-129">Dichiarare un puntatore a [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="7997d-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="7997d-130">Inizializzare il Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="7997d-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="7997d-131">Creare un'istanza di [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recuperare l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore.</span><span class="sxs-lookup"><span data-stu-id="7997d-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="7997d-132">La funzione di esempio seguente inizializza COM e quindi crea l'oggetto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , recuperando l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore *ppAutomation* .</span><span class="sxs-lookup"><span data-stu-id="7997d-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="7997d-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7997d-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7997d-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7997d-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7997d-135">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7997d-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="7997d-136">Ottenere elementi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="7997d-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 
---
title: Interfaccia IAccessibleEx
description: I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft, ma che implementano IAccessible, possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente implementando l'interfaccia IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116885"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="f0331-103">Interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="f0331-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="f0331-104">I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft, ma che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="f0331-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="f0331-105">Questa interfaccia consente al controllo di esporre le proprietà e i pattern di controllo di automazione interfaccia utente senza la necessità di un'implementazione completa delle interfacce del provider di automazione interfaccia utente, ad esempio [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="f0331-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="f0331-106">Per usare **IAccessibleEx**, **IRawElementProviderFragment** e tutte le altre interfacce di automazione interfaccia utente, includere il file di intestazione UIAutomation. h nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f0331-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="f0331-107">Si consideri, ad esempio, un controllo personalizzato con un valore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="f0331-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="f0331-108">Il server Microsoft Active Accessibility per il controllo definisce il ruolo del controllo ed è in grado di restituire il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="f0331-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="f0331-109">Tuttavia, poiché Microsoft Active Accessibility non definisce le proprietà minime e massime, il server non dispone dei mezzi per restituire i valori minimo e massimo del controllo.</span><span class="sxs-lookup"><span data-stu-id="f0331-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="f0331-110">Un client di automazione interfaccia utente è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà di Active Accessibility Microsoft, perché il nucleo di automazione interfaccia utente può ottenere tali proprietà tramite [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="f0331-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="f0331-111">Tuttavia, senza l'accesso a un'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sull'oggetto, l'automazione dell'interfaccia utente non è in grado di recuperare i valori massimi e minimi.</span><span class="sxs-lookup"><span data-stu-id="f0331-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="f0331-112">Lo sviluppatore del controllo può fornire un provider di automazione interfaccia utente completo per il controllo, ma ciò comporta la duplicazione di gran parte delle funzionalità esistenti dell'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ad esempio la navigazione e le proprietà comuni.</span><span class="sxs-lookup"><span data-stu-id="f0331-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="f0331-113">Lo sviluppatore può invece continuare a basarsi su **IAccessible** per fornire questa funzionalità, aggiungendo il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="f0331-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0331-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f0331-114">In this section</span></span>

-   [<span data-ttu-id="f0331-115">Linee guida per l'implementazione di IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="f0331-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="f0331-116">Implementazione di IAccessibleEx per i provider</span><span class="sxs-lookup"><span data-stu-id="f0331-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="f0331-117">Uso di IAccessibleEx da un client</span><span class="sxs-lookup"><span data-stu-id="f0331-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="f0331-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0331-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0331-119">Infrastruttura comune</span><span class="sxs-lookup"><span data-stu-id="f0331-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 





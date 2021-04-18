---
title: Procedure consigliate per l'utilizzo di matrici sicure
description: Molti metodi di interfaccia di automazione interfaccia utente Microsoft \ 32; API accettano gli argomenti chiamati matrici sicure del tipo di dati SAFEARRAY. In questo argomento vengono descritte le procedure consigliate per l'utilizzo di matrici sicure in un'applicazione di automazione interfaccia utente.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automazione interfaccia utente, matrici sicure
- Automazione interfaccia utente, provider
- Automazione interfaccia utente, client
- Automazione interfaccia utente, conversione tra tipi di dati
- client, matrici sicure
- provider, automazione interfaccia utente
- matrici sicure
- tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300169"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="796cd-112">Procedure consigliate per l'utilizzo di matrici sicure</span><span class="sxs-lookup"><span data-stu-id="796cd-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="796cd-113">Molti metodi di interfaccia dell'API di automazione interfaccia utente Microsoft accettano gli argomenti chiamati matrici sicure del tipo di dati [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="796cd-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="796cd-114">In questo argomento vengono descritte le procedure consigliate per l'utilizzo di matrici sicure in un'applicazione di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="796cd-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="796cd-115">Client</span><span class="sxs-lookup"><span data-stu-id="796cd-115">Clients</span></span>

<span data-ttu-id="796cd-116">Tutte le matrici sicure usate con i metodi dell'API client di automazione interfaccia utente sono matrici unidimensionali in base zero.</span><span class="sxs-lookup"><span data-stu-id="796cd-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="796cd-117">Per creare una matrice sicura per un metodo client di automazione interfaccia utente, usare la funzione [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) e per leggere e scrivere in una matrice sicura, usare le funzioni [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) e [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="796cd-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="796cd-118">Al termine dell'uso di un array sicuro, eliminarlo sempre usando la funzione [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , se è stata creata la matrice sicura o ricevuta da un metodo client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="796cd-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="796cd-119">Diversi metodi di automazione interfaccia utente, inclusi i metodi di recupero delle proprietà, ad esempio [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperano le [**varianti**](/windows/win32/api/oaidl/ns-oaidl-variant)che possono contenere strutture [**Point**](/previous-versions//dd162805(v=vs.85)) o [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) .</span><span class="sxs-lookup"><span data-stu-id="796cd-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="796cd-120">Un **punto** viene compresso in una **variante** come una matrice sicura di doppi (VT \_ R8) con il membro **x** in corrispondenza dell'indice 0 e il membro **y** in corrispondenza dell'indice 1.</span><span class="sxs-lookup"><span data-stu-id="796cd-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="796cd-121">Analogamente, un **UiaRect** viene compresso in una **variante** come matrice sicura di Double con i membri **Left**, **Top**, **Width** e **Height** rispettivamente negli indici da 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="796cd-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="796cd-122">Per una matrice di strutture **UiaRect** , la matrice sicura contiene una matrice sequenziale di quattro doppi per ogni **UiaRect**.</span><span class="sxs-lookup"><span data-stu-id="796cd-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="796cd-123">I membri **Left**, **Top**, **Width** e **Height** del primo **UiaRect** occupano l'indice da 0 a 3, i membri del secondo rettangolo occupano l'indice da 4 a 7 e così via.</span><span class="sxs-lookup"><span data-stu-id="796cd-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="796cd-124">L'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) include i metodi seguenti per la conversione tra [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) e diversi altri tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="796cd-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="796cd-125">Metodo</span><span class="sxs-lookup"><span data-stu-id="796cd-125">Method</span></span>                                                                                               | <span data-ttu-id="796cd-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="796cd-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="796cd-127">**IUIAutomation::IntNativeArrayToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="796cd-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="796cd-128">Converte una matrice di numeri interi in un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="796cd-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="796cd-129">**IUIAutomation::IntSafeArrayToNativeArray**</span><span class="sxs-lookup"><span data-stu-id="796cd-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="796cd-130">Converte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di interi in una matrice.</span><span class="sxs-lookup"><span data-stu-id="796cd-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="796cd-131">**IUIAutomation::SafeArrayToRectNativeArray**</span><span class="sxs-lookup"><span data-stu-id="796cd-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="796cd-132">Converte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) che contiene Coordinate rettangolo in una matrice di tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="796cd-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="796cd-133">Provider</span><span class="sxs-lookup"><span data-stu-id="796cd-133">Providers</span></span>

<span data-ttu-id="796cd-134">Un provider deve implementare una serie di metodi di interfaccia chiamati da automazione interfaccia utente per recuperare le informazioni dal provider.</span><span class="sxs-lookup"><span data-stu-id="796cd-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="796cd-135">Molte volte tali informazioni sono costituite da una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="796cd-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="796cd-136">Per restituire una matrice all'automazione interfaccia utente, il provider deve comprimere la matrice in una struttura [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="796cd-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="796cd-137">Gli elementi della matrice devono essere del tipo di dati previsto e devono essere visualizzati nell'ordine previsto.</span><span class="sxs-lookup"><span data-stu-id="796cd-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="796cd-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="796cd-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="796cd-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="796cd-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="796cd-140">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="796cd-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="796cd-141">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="796cd-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 
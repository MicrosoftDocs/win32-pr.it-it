---
title: Linee guida per COM e Unicode
description: Poiché Microsoft Active Accessibility si basa su Component Object Model (COM), gli sviluppatori hanno bisogno di un livello moderato di informazioni sugli oggetti e sulle interfacce COM e devono sapere come eseguire le attività di base, ad esempio come inizializzare la libreria COM.
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299936"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="984cb-103">Linee guida per COM e Unicode</span><span class="sxs-lookup"><span data-stu-id="984cb-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="984cb-104">Poiché Microsoft Active Accessibility si basa su Component Object Model (COM), gli sviluppatori hanno bisogno di un livello moderato di informazioni sugli oggetti e sulle interfacce COM e devono sapere come eseguire le attività di base, ad esempio come inizializzare la libreria COM.</span><span class="sxs-lookup"><span data-stu-id="984cb-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="984cb-105">Gli sviluppatori di server devono comprendere come progettare classi che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e come creare oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="984cb-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="984cb-106">È anche necessario un livello moderato di informazioni su Unicode per usare molte delle funzioni di Microsoft Active Accessibility che restituiscono stringhe.</span><span class="sxs-lookup"><span data-stu-id="984cb-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="984cb-107">Per utilizzare Microsoft Active Accessibility in modo efficace, è necessario comprendere le funzioni, le strutture, i tipi di dati e le interfacce COM e Unicode seguenti.</span><span class="sxs-lookup"><span data-stu-id="984cb-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="984cb-108">In questa documentazione vengono fornite informazioni limitate su alcuni di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="984cb-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="984cb-109">Funzioni:</span><span class="sxs-lookup"><span data-stu-id="984cb-109">Functions:</span></span>

-   [<span data-ttu-id="984cb-110">**OleInitialize**</span><span class="sxs-lookup"><span data-stu-id="984cb-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="984cb-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="984cb-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="984cb-112">[**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="984cb-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="984cb-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="984cb-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="984cb-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="984cb-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="984cb-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="984cb-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="984cb-116">Strutture e tipi di dati:</span><span class="sxs-lookup"><span data-stu-id="984cb-116">Structures and data types:</span></span>

-   [<span data-ttu-id="984cb-117">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="984cb-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="984cb-118">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="984cb-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="984cb-119">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="984cb-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="984cb-120">Interfacce COM:</span><span class="sxs-lookup"><span data-stu-id="984cb-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="984cb-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="984cb-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="984cb-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="984cb-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="984cb-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="984cb-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="984cb-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="984cb-124">In this section</span></span>

-   [<span data-ttu-id="984cb-125">Struttura VARIANT</span><span class="sxs-lookup"><span data-stu-id="984cb-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="984cb-126">IDispatch (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="984cb-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="984cb-127">Conversione di stringhe Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="984cb-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 
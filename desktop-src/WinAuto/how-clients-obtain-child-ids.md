---
title: Come i client ottengono gli ID figlio
description: Come i client ottengono gli ID figlio
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727722"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="12ecd-103">Come i client ottengono gli ID figlio</span><span class="sxs-lookup"><span data-stu-id="12ecd-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="12ecd-104">Gli sviluppatori client possono ottenere l'ID figlio di un oggetto nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="12ecd-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="12ecd-105">Chiamare [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span><span class="sxs-lookup"><span data-stu-id="12ecd-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="12ecd-106">Questa funzione recupera una matrice di strutture [**Variant**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="12ecd-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="12ecd-107">Eseguire una query sull'oggetto per verificare se supporta l'interfaccia [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="12ecd-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="12ecd-108">Se è presente, utilizzare [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) per ottenere gli ID figlio.</span><span class="sxs-lookup"><span data-stu-id="12ecd-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="12ecd-109">Raccogliere gli ID figlio chiamando il metodo [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="12ecd-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="12ecd-110">È responsabilità del client liberare la memoria usata per le strutture [**Variant**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="12ecd-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="12ecd-111">I client devono inoltre chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su qualsiasi interfaccia [**IDispatch**](idispatch-interface.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="12ecd-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 
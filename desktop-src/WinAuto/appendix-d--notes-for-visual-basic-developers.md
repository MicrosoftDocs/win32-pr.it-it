---
title: Appendice D Note per gli sviluppatori di Visual Basic
description: In questa sezione vengono fornite informazioni su Microsoft Active Accessibility per sviluppatori Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955414"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="f46df-103">Appendice D: Note per gli sviluppatori di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f46df-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="f46df-104">In questa sezione vengono fornite informazioni su Microsoft Active Accessibility per sviluppatori Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f46df-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="f46df-105">Le applicazioni scritte in Visual Basic sono client Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="f46df-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="f46df-106">Non forniscono informazioni sugli elementi dell'interfaccia utente personalizzati perché non implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o qualsiasi altra interfaccia Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="f46df-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="f46df-107">In questa documentazione vengono utilizzati i nomi C/C++ per le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Tuttavia, i nomi di Visual Basic sono simili.</span><span class="sxs-lookup"><span data-stu-id="f46df-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="f46df-108">Ad esempio, la proprietà [**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) viene chiamata **accName** in un'applicazione Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f46df-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f46df-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f46df-109">In this section</span></span>

-   [<span data-ttu-id="f46df-110">Note sul metodo Visual Basic: accName</span><span class="sxs-lookup"><span data-stu-id="f46df-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="f46df-111">Note sul metodo Visual Basic: accValue</span><span class="sxs-lookup"><span data-stu-id="f46df-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="f46df-112">Visual Basic programmi di esempio</span><span class="sxs-lookup"><span data-stu-id="f46df-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 





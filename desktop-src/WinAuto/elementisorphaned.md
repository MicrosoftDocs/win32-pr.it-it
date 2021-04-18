---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298961"
---
# <a name="elementisorphaned"></a><span data-ttu-id="1c4a6-103">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="1c4a6-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="1c4a6-104">Testo</span><span class="sxs-lookup"><span data-stu-id="1c4a6-104">Text</span></span>

<span data-ttu-id="1c4a6-105">L'elemento è un oggetto IAccessible orfano nell'albero</span><span class="sxs-lookup"><span data-stu-id="1c4a6-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="1c4a6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c4a6-106">Type</span></span>

<span data-ttu-id="1c4a6-107">Errore</span><span class="sxs-lookup"><span data-stu-id="1c4a6-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="1c4a6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c4a6-108">Description</span></span>

<span data-ttu-id="1c4a6-109">L'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="1c4a6-110">Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="1c4a6-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="1c4a6-111">Possible causes</span></span>

-   <span data-ttu-id="1c4a6-112">Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="1c4a6-113">Implementazione MSAA non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="1c4a6-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c4a6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c4a6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c4a6-115">Navigazione tramite hit testing e posizione dello schermo</span><span class="sxs-lookup"><span data-stu-id="1c4a6-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="1c4a6-116">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="1c4a6-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 





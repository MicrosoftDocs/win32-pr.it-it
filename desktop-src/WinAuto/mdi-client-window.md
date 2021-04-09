---
title: Finestra client MDI (riferimento all'elemento MSAA UI)
description: L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows. Un'applicazione MDI consente a un utente di usare più di un documento alla volta.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955426"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="69a92-104">Finestra client MDI (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="69a92-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="69a92-105">L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows.</span><span class="sxs-lookup"><span data-stu-id="69a92-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="69a92-106">Un'applicazione MDI consente a un utente di usare più di un documento alla volta.</span><span class="sxs-lookup"><span data-stu-id="69a92-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="69a92-107">Un'applicazione MDI dispone di tre tipi di finestre: una finestra cornice, una finestra client e un numero di finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="69a92-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="69a92-108">La finestra cornice è simile alla finestra principale di un'applicazione e racchiude la finestra del client.</span><span class="sxs-lookup"><span data-stu-id="69a92-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="69a92-109">La finestra del client è un elemento figlio della finestra cornice e funge da sfondo per le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="69a92-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="69a92-110">La finestra client fornisce inoltre supporto per la creazione e la modifica delle finestre figlio in cui vengono visualizzati i documenti.</span><span class="sxs-lookup"><span data-stu-id="69a92-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="69a92-111">Il nome della classe di finestra per una finestra client MDI è "MDIClient".</span><span class="sxs-lookup"><span data-stu-id="69a92-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="69a92-112">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="69a92-112">IAccessible Methods</span></span>

<span data-ttu-id="69a92-113">Una finestra client MDI supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="69a92-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="69a92-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="69a92-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="69a92-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="69a92-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="69a92-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="69a92-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="69a92-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="69a92-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="69a92-118">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="69a92-118">IAccessible Properties</span></span>

<span data-ttu-id="69a92-119">Una finestra client MDI supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="69a92-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="69a92-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69a92-120">Property</span></span>                                                                 | <span data-ttu-id="69a92-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="69a92-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69a92-122">**ottenere \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="69a92-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="69a92-123">La proprietà **childCount** è il numero di finestre figlio in cui vengono visualizzati i documenti.</span><span class="sxs-lookup"><span data-stu-id="69a92-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="69a92-124">**ottenere \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="69a92-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="69a92-125">**ottenere \_ accName**</span><span class="sxs-lookup"><span data-stu-id="69a92-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="69a92-126">La proprietà **Name** è "Workspace".</span><span class="sxs-lookup"><span data-stu-id="69a92-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="69a92-127">**ottenere \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="69a92-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="69a92-128">La proprietà **Parent** è la finestra cornice MDI.</span><span class="sxs-lookup"><span data-stu-id="69a92-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="69a92-129">**ottenere \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="69a92-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="69a92-130">La proprietà **Role** è [**un \_ \_ client di sistema del ruolo**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="69a92-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="69a92-131">**ottenere \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="69a92-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="69a92-132">**ottenere \_ accState**</span><span class="sxs-lookup"><span data-stu-id="69a92-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="69a92-133">La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile</span><span class="sxs-lookup"><span data-stu-id="69a92-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="69a92-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69a92-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a92-135">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="69a92-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






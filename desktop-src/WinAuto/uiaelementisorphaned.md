---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298383"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="48757-103">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="48757-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="48757-104">Testo</span><span class="sxs-lookup"><span data-stu-id="48757-104">Text</span></span>

<span data-ttu-id="48757-105">L'elemento è un oggetto AutomationElement orfano nell'albero</span><span class="sxs-lookup"><span data-stu-id="48757-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="48757-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="48757-106">Type</span></span>

<span data-ttu-id="48757-107">Errore</span><span class="sxs-lookup"><span data-stu-id="48757-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="48757-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48757-108">Description</span></span>

<span data-ttu-id="48757-109">L'indirizzo dell'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="48757-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="48757-110">Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.</span><span class="sxs-lookup"><span data-stu-id="48757-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="48757-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="48757-111">Possible causes</span></span>

-   <span data-ttu-id="48757-112">Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.</span><span class="sxs-lookup"><span data-stu-id="48757-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="48757-113">Implementazione di automazione interfaccia utente non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="48757-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48757-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48757-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48757-115">**IUIAutomationElement.ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="48757-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 





---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046967"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="6433a-103">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="6433a-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="6433a-104">Testo</span><span class="sxs-lookup"><span data-stu-id="6433a-104">Text</span></span>

<span data-ttu-id="6433a-105">La tabulazione in questa applicazione non è ciclica.</span><span class="sxs-lookup"><span data-stu-id="6433a-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="6433a-106">Il tabulazione in avanti o indietro {0} volte non torna allo stesso controllo.</span><span class="sxs-lookup"><span data-stu-id="6433a-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="6433a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6433a-107">Type</span></span>

<span data-ttu-id="6433a-108">Errore</span><span class="sxs-lookup"><span data-stu-id="6433a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6433a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6433a-109">Description</span></span>

<span data-ttu-id="6433a-110">Quando si usa la navigazione da tastiera standard (TAB o MAIUSC + TAB), non è possibile attraversare la struttura ad albero degli elementi della destinazione di verifica finché l'elemento iniziale diventa l'elemento finale (usando lo stesso numero di sequenze di tasti) invertendo la direzione di attraversamento.</span><span class="sxs-lookup"><span data-stu-id="6433a-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="6433a-111">Ad esempio, la tabulazione in avanti (tabulazione) x volte dall'elemento A (0) all'elemento A (x) e la tabulazione indietro (MAIUSC + TAB) x volte non determinano il riattivazione dell'elemento A (0).</span><span class="sxs-lookup"><span data-stu-id="6433a-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="6433a-112">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché non esiste un modo prevedibile per tornare a un controllo dopo che è stato visitato.</span><span class="sxs-lookup"><span data-stu-id="6433a-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6433a-113">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="6433a-113">Possible causes</span></span>

-   <span data-ttu-id="6433a-114">L'elemento o il relativo padre è un controllo personalizzato che non implementa correttamente la tabulazione.</span><span class="sxs-lookup"><span data-stu-id="6433a-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="6433a-115">Ad esempio, la proprietà stato MSAA non è impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="6433a-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="6433a-116">Alcune applicazioni, ad esempio il blocco note, presentano questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="6433a-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6433a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6433a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6433a-118">Linee guida per la progettazione dell'interfaccia utente della tastiera</span><span class="sxs-lookup"><span data-stu-id="6433a-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 
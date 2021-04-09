---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117986"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="79237-103">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="79237-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="79237-104">Testo</span><span class="sxs-lookup"><span data-stu-id="79237-104">Text</span></span>

<span data-ttu-id="79237-105">La tabulazione all'indietro e in avanti non produce lo stesso elemento.</span><span class="sxs-lookup"><span data-stu-id="79237-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="79237-106">Prevista {0} ma ricevuta {1}</span><span class="sxs-lookup"><span data-stu-id="79237-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="79237-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="79237-107">Type</span></span>

<span data-ttu-id="79237-108">Errore</span><span class="sxs-lookup"><span data-stu-id="79237-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="79237-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79237-109">Description</span></span>

<span data-ttu-id="79237-110">Quando si usa la navigazione da tastiera standard (TAB o MAIUSC + TAB), non è possibile ripetere il percorso di attraversamento attraverso l'albero degli elementi della destinazione di verifica se la direzione di attraversamento è invertita.</span><span class="sxs-lookup"><span data-stu-id="79237-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="79237-111">Ad esempio, la tabulazione in avanti (tabulazione) x volte dall'elemento A (0) all'elemento A (x) e quindi alla tabulazione indietro (MAIUSC + TAB) x volte genera l'elemento A (0) riottenendo lo stato attivo tramite un set di elementi intermedi diverso.</span><span class="sxs-lookup"><span data-stu-id="79237-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="79237-112">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché gli elementi attraversati sembrano imprevedibili e imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="79237-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="79237-113">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="79237-113">Possible causes</span></span>

-   <span data-ttu-id="79237-114">Più elementi o i relativi padri sono controlli personalizzati che non implementano correttamente la tabulazione.</span><span class="sxs-lookup"><span data-stu-id="79237-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="79237-115">Ad esempio, la proprietà stato MSAA non è impostata correttamente.</span><span class="sxs-lookup"><span data-stu-id="79237-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79237-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79237-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79237-117">Linee guida per la progettazione dell'interfaccia utente della tastiera</span><span class="sxs-lookup"><span data-stu-id="79237-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 
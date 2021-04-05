---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727519"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="a71df-103">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="a71df-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="a71df-104">Testo</span><span class="sxs-lookup"><span data-stu-id="a71df-104">Text</span></span>

<span data-ttu-id="a71df-105">Questo elemento sembra essere a schede, ma non è nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a71df-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="a71df-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71df-106">Type</span></span>

<span data-ttu-id="a71df-107">Errore</span><span class="sxs-lookup"><span data-stu-id="a71df-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a71df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a71df-108">Description</span></span>

<span data-ttu-id="a71df-109">Non è possibile accedere A un elemento attivabile mediante la navigazione da tastiera standard (TAB o MAIUSC + TAB).</span><span class="sxs-lookup"><span data-stu-id="a71df-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="a71df-110">Ad esempio, l'elemento non è stato contrassegnato come tabulazione o è stato assegnato un indice di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a71df-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="a71df-111">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché:</span><span class="sxs-lookup"><span data-stu-id="a71df-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="a71df-112">L'elemento non è individuabile.</span><span class="sxs-lookup"><span data-stu-id="a71df-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="a71df-113">Se l'elemento è figlio di un controllo elenco personalizzato, i segnali che indicano l'elemento figlio possono essere spostati utilizzando la freccia o i tasti di pagina potrebbero essere mancanti.</span><span class="sxs-lookup"><span data-stu-id="a71df-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a71df-114">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="a71df-114">Possible causes</span></span>

-   <span data-ttu-id="a71df-115">Il ruolo MSAA dell'elemento o del relativo elemento padre non è impostato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a71df-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="a71df-116">Se, ad esempio, tutti gli elementi dell'elenco in un controllo di visualizzazione elenco non vengono esposti tramite MSAA come oggetto \_ ListItem del sistema \_ del ruolo, la verifica non riesce perché le voci dell'elenco non sono accessibili tramite il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="a71df-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="a71df-117">L'elemento o il relativo padre è un controllo personalizzato che non implementa correttamente la tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a71df-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="a71df-118">Ad esempio, la proprietà dello stato MSAA non è mai impostata su stato di attivazione del sistema di stato \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a71df-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="a71df-119">Un elemento che funge da contenitore per altri elementi è stato selezionato per la verifica ma non supporta la navigazione da tastiera.</span><span class="sxs-lookup"><span data-stu-id="a71df-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="a71df-120">Ad esempio, una barra degli strumenti e i relativi elementi figlio non sono accessibili utilizzando il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="a71df-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a71df-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a71df-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a71df-122">Linee guida per la progettazione dell'interfaccia utente della tastiera</span><span class="sxs-lookup"><span data-stu-id="a71df-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 
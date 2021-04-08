---
title: Barra di scorrimento semplice
description: Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855714"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="c103f-103">Barra di scorrimento semplice</span><span class="sxs-lookup"><span data-stu-id="c103f-103">Flat Scroll Bar</span></span>

<span data-ttu-id="c103f-104">Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="c103f-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="c103f-105">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="c103f-105">Overviews</span></span>



| <span data-ttu-id="c103f-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="c103f-106">Topic</span></span>                                    | <span data-ttu-id="c103f-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="c103f-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c103f-108">Barre di scorrimento Flat</span><span class="sxs-lookup"><span data-stu-id="c103f-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="c103f-109">In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici.</span><span class="sxs-lookup"><span data-stu-id="c103f-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="c103f-110">Dal punto di vista funzionale, le barre di scorrimento Flat funzionano esattamente come le barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="c103f-111">La differenza consiste nel fatto che è possibile personalizzare l'aspetto in modo più ampio rispetto alle barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="c103f-112">Funzioni</span><span class="sxs-lookup"><span data-stu-id="c103f-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c103f-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="c103f-113">Topic</span></span></th>
<th><span data-ttu-id="c103f-114">Contenuto</span><span class="sxs-lookup"><span data-stu-id="c103f-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c103f-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="c103f-116">Abilita o Disabilita uno o entrambi i pulsanti di direzione della barra di scorrimento flat.</span><span class="sxs-lookup"><span data-stu-id="c103f-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="c103f-117">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="c103f-119">Ottiene le informazioni per una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="c103f-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="c103f-120">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="c103f-122">Ottiene la posizione del cursore in una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="c103f-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="c103f-123">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="c103f-125">Ottiene le proprietà per una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="c103f-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="c103f-126">Questa funzione può essere usata anche per determinare se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> è stato chiamato per questa finestra.</span><span class="sxs-lookup"><span data-stu-id="c103f-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="c103f-128">Ottiene le proprietà per una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="c103f-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="c103f-129">Questa funzione può essere usata anche per determinare se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> è stato chiamato per questa finestra.</span><span class="sxs-lookup"><span data-stu-id="c103f-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c103f-130">Questo è identico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c103f-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="c103f-132">Ottiene l'intervallo di scorrimento per una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="c103f-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="c103f-133">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="c103f-135">Imposta le informazioni per una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="c103f-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="c103f-136">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="c103f-138">Imposta la posizione corrente del cursore in una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="c103f-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="c103f-139">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="c103f-141">Imposta le proprietà per una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="c103f-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="c103f-143">Imposta l'intervallo di scorrimento di una barra di scorrimento piatta.</span><span class="sxs-lookup"><span data-stu-id="c103f-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="c103f-144">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="c103f-146">Mostra o nasconde una barra di scorrimento semplice.</span><span class="sxs-lookup"><span data-stu-id="c103f-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="c103f-147">Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c103f-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="c103f-149">Inizializza le barre di scorrimento flat per una particolare finestra.</span><span class="sxs-lookup"><span data-stu-id="c103f-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c103f-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span><span class="sxs-lookup"><span data-stu-id="c103f-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="c103f-151">Consente di inizializzare le barre di scorrimento flat per una particolare finestra.</span><span class="sxs-lookup"><span data-stu-id="c103f-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="c103f-152">La finestra specificata verrà ripristinata sulle barre di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="c103f-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 






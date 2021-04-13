---
title: Barra del titolo (riferimento all'elemento MSAA UI)
description: La barra del titolo nella parte superiore di una finestra Visualizza un'icona definita dall'applicazione e una riga di testo.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398492"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="d359c-103">Barra del titolo (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="d359c-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="d359c-104">Questo argomento descrive gli oggetti della **barra del titolo** a scopo di riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="d359c-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="d359c-105">La creazione di oggetti della **barra del titolo** in diversi framework dell'interfaccia utente non è descritta qui.</span><span class="sxs-lookup"><span data-stu-id="d359c-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="d359c-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="d359c-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="d359c-107">La barra del titolo nella parte superiore di una finestra Visualizza un'icona definita dall'applicazione e una riga di testo.</span><span class="sxs-lookup"><span data-stu-id="d359c-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="d359c-108">Il testo specifica il nome dell'applicazione e indica lo scopo della finestra.</span><span class="sxs-lookup"><span data-stu-id="d359c-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="d359c-109">La barra del titolo consente inoltre all'utente di spostare la finestra utilizzando un mouse o un altro dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="d359c-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="d359c-110">Le barre del titolo contengono almeno tre piccoli pulsanti che consentono di ridurre al minimo, ingrandire o ripristinare e chiudere la finestra associata alla barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d359c-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="d359c-111">Le barre del titolo contengono anche un pulsante della Guida sensibile al contesto.</span><span class="sxs-lookup"><span data-stu-id="d359c-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="d359c-112">Le applicazioni in esecuzione nella versione Far-East del sistema operativo Windows possono contenere anche pulsanti input Method Editor (IME).</span><span class="sxs-lookup"><span data-stu-id="d359c-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="d359c-113">Microsoft Active Accessibility espone questi pulsanti come elementi figlio della barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d359c-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="d359c-114">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="d359c-114">IAccessible Methods</span></span>

<span data-ttu-id="d359c-115">Le barre del titolo supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="d359c-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="d359c-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="d359c-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="d359c-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="d359c-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="d359c-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="d359c-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="d359c-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="d359c-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="d359c-120">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="d359c-120">IAccessible Properties</span></span>

<span data-ttu-id="d359c-121">Le barre del titolo supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="d359c-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d359c-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d359c-122">Property</span></span></th>
<th><span data-ttu-id="d359c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d359c-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d359c-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="d359c-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="d359c-125">La proprietà <strong>childCount</strong> è cinque.</span><span class="sxs-lookup"><span data-stu-id="d359c-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="d359c-126">La proprietà <strong>childCount</strong> include i pulsanti IME e Guida sensibile al contesto anche quando non sono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="d359c-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="d359c-127">I pulsanti che non sono visualizzati hanno la proprietà <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d359c-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d359c-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="d359c-129">La proprietà <strong>Description</strong> della barra del titolo è: &quot; Visualizza il nome della finestra e contiene i controlli per modificarla. &quot; I pulsanti figlio nella barra del titolo presentano le descrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d359c-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="d359c-130">&quot;Sposta la finestra da</span><span class="sxs-lookup"><span data-stu-id="d359c-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="d359c-131">&quot;Rende la finestra completa</span><span class="sxs-lookup"><span data-stu-id="d359c-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="d359c-132">&quot;Inserisce un oggetto ridotto a icona o</span><span class="sxs-lookup"><span data-stu-id="d359c-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="d359c-133">&quot;Chiude la finestra&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="d359c-134">&quot;Entra o lascia il contesto-</span><span class="sxs-lookup"><span data-stu-id="d359c-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="d359c-135">&quot;Visualizza la tastiera quando viene premuto&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d359c-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="d359c-137">La barra del titolo non supporta la proprietà <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="d359c-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="d359c-138">I pulsanti figlio nella barra del titolo hanno i nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d359c-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="d359c-139">&quot;Riduci&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="d359c-140">&quot;Ingrandisci &quot; o &quot; Ripristina &quot; ,</span><span class="sxs-lookup"><span data-stu-id="d359c-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="d359c-141">&quot;Close&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="d359c-142">&quot;Guida del contesto&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="d359c-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="d359c-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d359c-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="d359c-145">La proprietà <strong>Parent</strong> della barra del titolo è la finestra principale dell'applicazione ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) con lo stesso nome della classe di finestra definito dall'applicazione della barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d359c-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d359c-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="d359c-147">La proprietà <strong>Role</strong> è <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d359c-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="d359c-148">I pulsanti figlio nella barra del titolo hanno la <strong></strong> proprietà Role <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d359c-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d359c-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="d359c-150">La proprietà <strong>state</strong> per la barra del titolo e i pulsanti figlio possono essere una combinazione di uno o più dei <a href="object-state-constants.md">valori</a>seguenti: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="d359c-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d359c-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="d359c-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="d359c-152">La proprietà <strong>value</strong> è una stringa uguale al testo visualizzato nella barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d359c-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="d359c-153">Note</span><span class="sxs-lookup"><span data-stu-id="d359c-153">Notes</span></span>

-   <span data-ttu-id="d359c-154">Anche se la **barra del titolo** di un'applicazione ha lo stato del sistema di stato del flag di stato, lo **stato del flag di stato è** non [**\_ \_ attivo**](object-state-constants.md) [**\_ \_ .**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d359c-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="d359c-155">L'impostazione dello stato attivo su un oggetto della barra del titolo attiva la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d359c-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="d359c-156">Poiché l'oggetto barra del titolo non supporta [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), i pulsanti sulla barra del titolo sono elementi semplici.</span><span class="sxs-lookup"><span data-stu-id="d359c-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="d359c-157">Non supportano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="d359c-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="d359c-158">L'oggetto barra del titolo fornisce informazioni su questi pulsanti figlio.</span><span class="sxs-lookup"><span data-stu-id="d359c-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="d359c-159">Poiché le barre del titolo non ottengono lo stato attivo e non hanno un'azione predefinita, i metodi [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) e [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) non sono supportati per questo controllo.</span><span class="sxs-lookup"><span data-stu-id="d359c-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d359c-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d359c-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d359c-161">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="d359c-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






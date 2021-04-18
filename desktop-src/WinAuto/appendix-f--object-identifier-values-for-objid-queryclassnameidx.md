---
title: Appendice F valori identificatore oggetto per OBJID_QUERYCLASSNAMEIDX
description: Quando OLEACC Invia un \_ messaggio WM GetObject con il parametro lParam impostato su OBJIDQUERYCLASSNAMEIDX, molti controlli comuni o utente standard (COMCTL) restituiscono uno dei valori seguenti.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300185"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="28aa3-103">Appendice F: valori identificatore oggetto per OBJID \_ QUERYCLASSNAMEIDX</span><span class="sxs-lookup"><span data-stu-id="28aa3-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="28aa3-104">Quando OLEACC Invia un messaggio [**WM \_ GetObject**](wm-getobject.md) con il parametro *lParam* impostato su OBJIDQUERYCLASSNAMEIDX, molti controlli comuni o utente standard (COMCTL) restituiscono uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="28aa3-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="28aa3-105">UTENTE o controllo comune</span><span class="sxs-lookup"><span data-stu-id="28aa3-105">USER or common control</span></span> | <span data-ttu-id="28aa3-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28aa3-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="28aa3-107">ListBox</span><span class="sxs-lookup"><span data-stu-id="28aa3-107">Listbox</span></span>                | <span data-ttu-id="28aa3-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="28aa3-108">65536+0</span></span>      |
| <span data-ttu-id="28aa3-109">Pulsante</span><span class="sxs-lookup"><span data-stu-id="28aa3-109">Button</span></span>                 | <span data-ttu-id="28aa3-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="28aa3-110">65536+2</span></span>      |
| <span data-ttu-id="28aa3-111">Static</span><span class="sxs-lookup"><span data-stu-id="28aa3-111">Static</span></span>                 | <span data-ttu-id="28aa3-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="28aa3-112">65536+3</span></span>      |
| <span data-ttu-id="28aa3-113">Modifica</span><span class="sxs-lookup"><span data-stu-id="28aa3-113">Edit</span></span>                   | <span data-ttu-id="28aa3-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="28aa3-114">65536+4</span></span>      |
| <span data-ttu-id="28aa3-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="28aa3-115">Combobox</span></span>               | <span data-ttu-id="28aa3-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="28aa3-116">65536+5</span></span>      |
| <span data-ttu-id="28aa3-117">Barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="28aa3-117">Scrollbar</span></span>              | <span data-ttu-id="28aa3-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="28aa3-118">65536+10</span></span>     |
| <span data-ttu-id="28aa3-119">Stato</span><span class="sxs-lookup"><span data-stu-id="28aa3-119">Status</span></span>                 | <span data-ttu-id="28aa3-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="28aa3-120">65536+11</span></span>     |
| <span data-ttu-id="28aa3-121">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="28aa3-121">Toolbar</span></span>                | <span data-ttu-id="28aa3-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="28aa3-122">65536+12</span></span>     |
| <span data-ttu-id="28aa3-123">Avanzamento</span><span class="sxs-lookup"><span data-stu-id="28aa3-123">Progress</span></span>               | <span data-ttu-id="28aa3-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="28aa3-124">65536+13</span></span>     |
| <span data-ttu-id="28aa3-125">Animare</span><span class="sxs-lookup"><span data-stu-id="28aa3-125">Animate</span></span>                | <span data-ttu-id="28aa3-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="28aa3-126">65536+14</span></span>     |
| <span data-ttu-id="28aa3-127">Scheda</span><span class="sxs-lookup"><span data-stu-id="28aa3-127">Tab</span></span>                    | <span data-ttu-id="28aa3-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="28aa3-128">65536+15</span></span>     |
| <span data-ttu-id="28aa3-129">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="28aa3-129">Hotkey</span></span>                 | <span data-ttu-id="28aa3-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="28aa3-130">65536+16</span></span>     |
| <span data-ttu-id="28aa3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28aa3-131">Header</span></span>                 | <span data-ttu-id="28aa3-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="28aa3-132">65536+17</span></span>     |
| <span data-ttu-id="28aa3-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="28aa3-133">Trackbar</span></span>               | <span data-ttu-id="28aa3-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="28aa3-134">65536+18</span></span>     |
| <span data-ttu-id="28aa3-135">ListView</span><span class="sxs-lookup"><span data-stu-id="28aa3-135">Listview</span></span>               | <span data-ttu-id="28aa3-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="28aa3-136">65536+19</span></span>     |
| <span data-ttu-id="28aa3-137">UpDown</span><span class="sxs-lookup"><span data-stu-id="28aa3-137">Updown</span></span>                 | <span data-ttu-id="28aa3-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="28aa3-138">65536+22</span></span>     |
| <span data-ttu-id="28aa3-139">Descrizioni comandi</span><span class="sxs-lookup"><span data-stu-id="28aa3-139">ToolTips</span></span>               | <span data-ttu-id="28aa3-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="28aa3-140">65536+24</span></span>     |
| <span data-ttu-id="28aa3-141">TreeView</span><span class="sxs-lookup"><span data-stu-id="28aa3-141">Treeview</span></span>               | <span data-ttu-id="28aa3-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="28aa3-142">65536+25</span></span>     |
| <span data-ttu-id="28aa3-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="28aa3-143">RichEdit</span></span>               | <span data-ttu-id="28aa3-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="28aa3-144">65536+28</span></span>     |



 

<span data-ttu-id="28aa3-145">Solo gli utenti e i controlli comuni di Windows (COMCTL) restituiranno uno dei valori della tabella.</span><span class="sxs-lookup"><span data-stu-id="28aa3-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="28aa3-146">Se una finestra restituisce 0 in risposta a questo messaggio, la finestra può essere una delle seguenti:</span><span class="sxs-lookup"><span data-stu-id="28aa3-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="28aa3-147">Un controllo personalizzato</span><span class="sxs-lookup"><span data-stu-id="28aa3-147">A custom control</span></span>
-   <span data-ttu-id="28aa3-148">Controllo diverso da uno dei controlli della tabella precedente</span><span class="sxs-lookup"><span data-stu-id="28aa3-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="28aa3-149">Una versione precedente di un controllo di sistema che non riconosce il messaggio [**WM \_ GetObject**](wm-getobject.md)</span><span class="sxs-lookup"><span data-stu-id="28aa3-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="28aa3-150">Se una finestra restituisce 0, è possibile che i client debbano usare [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span><span class="sxs-lookup"><span data-stu-id="28aa3-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="28aa3-151">È possibile utilizzare queste funzioni per determinare il tipo di controllo in base al nome della classe.</span><span class="sxs-lookup"><span data-stu-id="28aa3-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="28aa3-152">In generale, i client possono usare le informazioni fornite da OLEACC.</span><span class="sxs-lookup"><span data-stu-id="28aa3-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 
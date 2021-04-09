---
title: Sottoclassi di controlli
description: Se un controllo esegue quasi tutte le operazioni desiderate, ma sono necessarie altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale eseguendo una sottoclasse.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047460"
---
# <a name="subclassing-controls"></a><span data-ttu-id="15e50-103">Sottoclassi di controlli</span><span class="sxs-lookup"><span data-stu-id="15e50-103">Subclassing Controls</span></span>

<span data-ttu-id="15e50-104">Se un controllo esegue quasi tutte le operazioni desiderate, ma sono necessarie altre funzionalità, è possibile modificare o aggiungere funzionalità al controllo originale eseguendo una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="15e50-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="15e50-105">Una sottoclasse può includere tutte le funzionalità di una classe esistente, oltre a tutte le funzionalità aggiuntive che si desidera assegnare.</span><span class="sxs-lookup"><span data-stu-id="15e50-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="15e50-106">Questo documento illustra come vengono create le sottoclassi e include gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="15e50-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="15e50-107">Controlli di sottoclasse prima della ComCtl32.dll versione 6</span><span class="sxs-lookup"><span data-stu-id="15e50-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="15e50-108">Archiviazione dei dati utente</span><span class="sxs-lookup"><span data-stu-id="15e50-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="15e50-109">Svantaggi del vecchio approccio di sottoclassi</span><span class="sxs-lookup"><span data-stu-id="15e50-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="15e50-110">Sottoclassi di controlli con ComCtl32.dll versione 6</span><span class="sxs-lookup"><span data-stu-id="15e50-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="15e50-111">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="15e50-112">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="15e50-113">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="15e50-114">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="15e50-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="15e50-115">Controlli di sottoclasse prima della ComCtl32.dll versione 6</span><span class="sxs-lookup"><span data-stu-id="15e50-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="15e50-116">È possibile inserire un controllo in una sottoclasse e archiviare i dati utente all'interno di un controllo.</span><span class="sxs-lookup"><span data-stu-id="15e50-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="15e50-117">Questa operazione viene eseguita quando si usano versioni di ComCtl32.dll precedenti alla versione 6.</span><span class="sxs-lookup"><span data-stu-id="15e50-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="15e50-118">La creazione di sottoclassi con versioni precedenti di ComCtl32.dll presenta alcuni svantaggi.</span><span class="sxs-lookup"><span data-stu-id="15e50-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="15e50-119">Per creare un nuovo controllo, è preferibile iniziare con uno dei controlli comuni di Windows ed estenderlo per adattarsi a una particolare esigenza.</span><span class="sxs-lookup"><span data-stu-id="15e50-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="15e50-120">Per estendere un controllo, creare un controllo e sostituire la relativa routine della finestra esistente con una nuova.</span><span class="sxs-lookup"><span data-stu-id="15e50-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="15e50-121">La nuova procedura intercetta i messaggi del controllo e li agisce o li passa alla procedura originale per l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="15e50-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="15e50-122">Utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) o [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) per sostituire l'oggetto WndProc del controllo.</span><span class="sxs-lookup"><span data-stu-id="15e50-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="15e50-123">Nell'esempio di codice seguente viene illustrato come sostituire un oggetto WNDPROC.</span><span class="sxs-lookup"><span data-stu-id="15e50-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="15e50-124">Archiviazione dei dati utente</span><span class="sxs-lookup"><span data-stu-id="15e50-124">Storing User Data</span></span>

<span data-ttu-id="15e50-125">Potrebbe essere necessario archiviare i dati utente con una singola finestra.</span><span class="sxs-lookup"><span data-stu-id="15e50-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="15e50-126">Questi dati possono essere utilizzati dalla nuova procedura della finestra per determinare come creare il controllo o dove inviare determinati messaggi.</span><span class="sxs-lookup"><span data-stu-id="15e50-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="15e50-127">Ad esempio, è possibile usare i dati per archiviare un puntatore di classe C++ alla classe che rappresenta il controllo.</span><span class="sxs-lookup"><span data-stu-id="15e50-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="15e50-128">Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**seprop**](/windows/desktop/api/winuser/nf-winuser-setpropa) per archiviare i dati con una finestra.</span><span class="sxs-lookup"><span data-stu-id="15e50-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="15e50-129">Svantaggi del vecchio approccio di sottoclassi</span><span class="sxs-lookup"><span data-stu-id="15e50-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="15e50-130">Nell'elenco seguente sono riportati alcuni degli svantaggi dell'utilizzo dell'approccio descritto in precedenza per la sottoclasse di un controllo.</span><span class="sxs-lookup"><span data-stu-id="15e50-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="15e50-131">La routine della finestra può essere sostituita solo una volta.</span><span class="sxs-lookup"><span data-stu-id="15e50-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="15e50-132">È difficile rimuovere una sottoclasse dopo che è stata creata.</span><span class="sxs-lookup"><span data-stu-id="15e50-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="15e50-133">L'associazione di dati privati a una finestra non è efficiente.</span><span class="sxs-lookup"><span data-stu-id="15e50-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="15e50-134">Per chiamare la procedura successiva in una catena di sottoclassi, non è possibile eseguire il cast della precedente routine della finestra e chiamarla, è necessario chiamarla tramite la funzione [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="15e50-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="15e50-135">Sottoclassi di controlli con ComCtl32.dll versione 6</span><span class="sxs-lookup"><span data-stu-id="15e50-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="15e50-136">ComCtl32.dll versione 6 è solo Unicode.</span><span class="sxs-lookup"><span data-stu-id="15e50-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="15e50-137">I controlli comuni supportati da ComCtl32.dll versione 6 non devono essere sottoclassati (o sottoclassati) con le routine della finestra ANSI.</span><span class="sxs-lookup"><span data-stu-id="15e50-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="15e50-138">ComCtl32.dll versione 6 contiene quattro funzioni che semplificano la creazione di sottoclassi ed eliminano gli svantaggi descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="15e50-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="15e50-139">Le nuove funzioni incapsulano la gestione di più set di dati di riferimento, pertanto lo sviluppatore può concentrarsi sulle funzionalità di programmazione e non sulla gestione delle sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="15e50-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="15e50-140">Le funzioni di sottoclasse sono:</span><span class="sxs-lookup"><span data-stu-id="15e50-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="15e50-141">**SetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="15e50-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="15e50-142">**GetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="15e50-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="15e50-143">**RemoveWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="15e50-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="15e50-144">**DefSubclassProc**</span><span class="sxs-lookup"><span data-stu-id="15e50-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="15e50-145">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-145">SetWindowSubclass</span></span>

<span data-ttu-id="15e50-146">Questa funzione viene utilizzata per eseguire inizialmente la sottoclasse di una finestra.</span><span class="sxs-lookup"><span data-stu-id="15e50-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="15e50-147">Ogni sottoclasse è identificata in modo univoco dall'indirizzo di *pfnSubclass* e del relativo *uIdSubclass*.</span><span class="sxs-lookup"><span data-stu-id="15e50-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="15e50-148">Entrambi sono parametri della funzione [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="15e50-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="15e50-149">Diverse sottoclassi possono condividere la stessa routine di sottoclasse e l'ID può identificare ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="15e50-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="15e50-150">Per modificare i dati di riferimento, è possibile effettuare chiamate successive a **SetWindowSubclass**.</span><span class="sxs-lookup"><span data-stu-id="15e50-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="15e50-151">Il vantaggio importante è che ogni istanza della sottoclasse ha i propri dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="15e50-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="15e50-152">La dichiarazione di una routine di sottoclasse è leggermente diversa da una routine normale della finestra perché contiene due elementi di dati aggiuntivi: l'ID della sottoclasse e i dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="15e50-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="15e50-153">Gli ultimi due parametri della dichiarazione di funzione seguente mostrano questo.</span><span class="sxs-lookup"><span data-stu-id="15e50-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="15e50-154">Ogni volta che un messaggio viene ricevuto dalla nuova procedura della finestra, vengono inclusi un ID sottoclasse e i dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="15e50-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="15e50-155">Tutte le stringhe passate alla routine sono stringhe Unicode anche se Unicode non è specificato come definizione del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="15e50-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="15e50-156">Nell'esempio seguente viene illustrata un'implementazione di scheletro di una routine della finestra per un controllo sottoclassato.</span><span class="sxs-lookup"><span data-stu-id="15e50-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="15e50-157">La procedura della finestra può essere associata al controllo nel gestore [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) della routine della finestra di dialogo, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="15e50-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="15e50-158">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-158">GetWindowSubclass</span></span>

<span data-ttu-id="15e50-159">Questa funzione recupera le informazioni su una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="15e50-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="15e50-160">Ad esempio, è possibile usare [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) per accedere ai dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="15e50-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="15e50-161">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="15e50-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="15e50-162">Questa funzione rimuove le sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="15e50-162">This function removes subclasses.</span></span> <span data-ttu-id="15e50-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combinazione con [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) consente di aggiungere e rimuovere in modo dinamico le sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="15e50-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="15e50-164">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="15e50-164">DefSubclassProc</span></span>

<span data-ttu-id="15e50-165">La funzione [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) chiama il gestore successivo nella catena di sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="15e50-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="15e50-166">La funzione recupera inoltre l'ID e i dati di riferimento appropriati e passa le informazioni alla successiva routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="15e50-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 
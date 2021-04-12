---
title: Proprietà KeyboardShortcut
description: La proprietà KeyboardShortcut descrive una combinazione di chiave o chiave che attiva un oggetto accessibile specificato.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221457"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="b4e8b-103">Proprietà KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="b4e8b-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="b4e8b-104">La proprietà **KeyboardShortcut** descrive una combinazione di chiave o chiave che attiva un oggetto accessibile specificato.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="b4e8b-105">La proprietà **KeyboardShortcut** viene recuperata chiamando [**IAccessible:: Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span><span class="sxs-lookup"><span data-stu-id="b4e8b-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="b4e8b-106">La stringa recuperata descrive un *tasto di scelta rapida* (detto anche tasto *di scelta rapida) o* un *tasto* di scelta (detto *anche tasto di scelta).*</span><span class="sxs-lookup"><span data-stu-id="b4e8b-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="b4e8b-107">Una chiave di accesso è un carattere sottolineato nel testo di un menu, di una voce di menu o di un'etichetta di un controllo, ad esempio un pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="b4e8b-108">La stringa recuperata deve contenere il nome della chiave insieme al tasto di modifica o alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="b4e8b-109">Il formato della stringa deve essere il seguente, in modo che i client possano analizzarlo facilmente: \[ \[ tasto di modifica... \] + \[ \] + \] nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="b4e8b-110">Gli esempi includono ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAIUSC + BACKSPACE o semplicemente BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="b4e8b-111">Nella tabella seguente sono elencati i tasti di modifica.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="b4e8b-112">Tasto di modifica</span><span class="sxs-lookup"><span data-stu-id="b4e8b-112">Modifier key</span></span> | <span data-ttu-id="b4e8b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4e8b-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="b4e8b-114">ALT</span><span class="sxs-lookup"><span data-stu-id="b4e8b-114">ALT</span></span>          | <span data-ttu-id="b4e8b-115">Tasto di modifica alternativo</span><span class="sxs-lookup"><span data-stu-id="b4e8b-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="b4e8b-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="b4e8b-116">CTRL</span></span>         | <span data-ttu-id="b4e8b-117">Tasto di modifica controllo</span><span class="sxs-lookup"><span data-stu-id="b4e8b-117">Control modifier key</span></span>               |
| <span data-ttu-id="b4e8b-118">MAIUSC</span><span class="sxs-lookup"><span data-stu-id="b4e8b-118">SHIFT</span></span>        | <span data-ttu-id="b4e8b-119">Tasto di modifica MAIUSC</span><span class="sxs-lookup"><span data-stu-id="b4e8b-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="b4e8b-120">WIN</span><span class="sxs-lookup"><span data-stu-id="b4e8b-120">WIN</span></span>          | <span data-ttu-id="b4e8b-121">Tasto logo Windows</span><span class="sxs-lookup"><span data-stu-id="b4e8b-121">Windows logo key</span></span>                   |
| <span data-ttu-id="b4e8b-122">FN</span><span class="sxs-lookup"><span data-stu-id="b4e8b-122">FN</span></span>           | <span data-ttu-id="b4e8b-123">Tasto funzione sui computer portatili</span><span class="sxs-lookup"><span data-stu-id="b4e8b-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="b4e8b-124">Non localizzare stringhe di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="b4e8b-125">Gestione di oggetti con entrambi i tipi di chiave</span><span class="sxs-lookup"><span data-stu-id="b4e8b-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="b4e8b-126">Se un oggetto ha sia un tasto di scelta rapida che una chiave di accesso, la proprietà **KeyboardShortcut** restituisce il tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="b4e8b-127">La chiave di accesso è quella che un utente preme quando l'oggetto o l'elemento padre dell'oggetto ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="b4e8b-128">Ad esempio, la voce di menu **stampa** potrebbe avere sia un tasto di scelta rapida (Ctrl + p) che un tasto di scelta (P).</span><span class="sxs-lookup"><span data-stu-id="b4e8b-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="b4e8b-129">Se un utente preme CTRL + P mentre il menu è attivo, non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="b4e8b-130">Tuttavia, se un utente preme P mentre il menu è attivo, richiama la finestra di dialogo **stampa** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="b4e8b-131">In questo caso, la proprietà **KeyboardShortcut** è "P" per riflettere gli elementi che l'utente deve premere quando il menu ha lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="b4e8b-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 





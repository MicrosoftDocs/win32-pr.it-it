---
title: Uso delle stringhe
description: .
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c74530a1acd0eb94f0d88662924203a8c58116
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117659"
---
# <a name="working-with-strings"></a><span data-ttu-id="ce531-103">Uso delle stringhe</span><span class="sxs-lookup"><span data-stu-id="ce531-103">Working with Strings</span></span>

<span data-ttu-id="ce531-104">Windows supporta in modo nativo le stringhe Unicode per gli elementi dell'interfaccia utente, i nomi di file e così via.</span><span class="sxs-lookup"><span data-stu-id="ce531-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="ce531-105">Unicode è la codifica dei caratteri preferita, perché supporta tutti i set di caratteri e le lingue.</span><span class="sxs-lookup"><span data-stu-id="ce531-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="ce531-106">Windows rappresenta i caratteri Unicode usando la codifica UTF-16, in cui ogni carattere viene codificato come valore a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ce531-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="ce531-107">I caratteri UTF-16 sono detti caratteri *Wide* per distinguerli da caratteri ANSI a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ce531-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="ce531-108">Il compilatore Visual C++ supporta il tipo di dati predefinito **WCHAR \_ t** per i caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="ce531-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="ce531-109">Il file di intestazione WinNT. h definisce anche il **typedef** seguente.</span><span class="sxs-lookup"><span data-stu-id="ce531-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="ce531-110">Vengono visualizzate entrambe le versioni nel codice di esempio MSDN.</span><span class="sxs-lookup"><span data-stu-id="ce531-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="ce531-111">Per dichiarare un valore letterale a caratteri wide o un valore letterale stringa di caratteri wide, inserire **L** prima del valore letterale.</span><span class="sxs-lookup"><span data-stu-id="ce531-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="ce531-112">Di seguito sono riportati alcuni altri typedef correlati a stringhe che verranno visualizzati:</span><span class="sxs-lookup"><span data-stu-id="ce531-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="ce531-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="ce531-113">Typedef</span></span>                   | <span data-ttu-id="ce531-114">Definizione</span><span class="sxs-lookup"><span data-stu-id="ce531-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="ce531-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="ce531-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="ce531-116">**Pstr** o **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="ce531-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="ce531-117">**PCSTR** o **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="ce531-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="ce531-118">**PWSTR** o **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ce531-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="ce531-119">**PCWSTR** o **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ce531-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="ce531-120">Funzioni Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ce531-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="ce531-121">Quando Microsoft ha introdotto il supporto Unicode per Windows, ha semplificato la transizione fornendo due set di API paralleli, uno per le stringhe ANSI e l'altro per le stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="ce531-122">Sono ad esempio disponibili due funzioni per impostare il testo della barra del titolo di una finestra:</span><span class="sxs-lookup"><span data-stu-id="ce531-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="ce531-123">**SetWindowTextA** accetta una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce531-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="ce531-124">**SetWindowTextW** accetta una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="ce531-125">Internamente, la versione ANSI converte la stringa in Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="ce531-126">Le intestazioni di Windows definiscono anche una macro che viene risolta nella versione Unicode quando viene definito il simbolo del preprocessore `UNICODE` o in caso contrario la versione ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce531-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="ce531-127">In MSDN, la funzione è documentata con il nome [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), anche se è effettivamente il nome della macro, non il nome effettivo della funzione.</span><span class="sxs-lookup"><span data-stu-id="ce531-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="ce531-128">Le nuove applicazioni devono sempre chiamare le versioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="ce531-129">Molti linguaggi internazionali richiedono Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-129">Many world languages require Unicode.</span></span> <span data-ttu-id="ce531-130">Se si usano stringhe ANSI, sarà impossibile localizzare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ce531-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="ce531-131">Anche le versioni ANSI sono meno efficienti perché il sistema operativo deve convertire le stringhe ANSI in Unicode in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ce531-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="ce531-132">A seconda delle preferenze, è possibile chiamare le funzioni Unicode in modo esplicito, ad esempio **SetWindowTextW**, oppure utilizzare le macro.</span><span class="sxs-lookup"><span data-stu-id="ce531-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="ce531-133">Il codice di esempio su MSDN chiama in genere le macro, ma le due forme sono esattamente equivalenti.</span><span class="sxs-lookup"><span data-stu-id="ce531-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="ce531-134">Le API più recenti in Windows hanno solo una versione Unicode, senza alcuna versione ANSI corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ce531-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="ce531-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="ce531-135">TCHARs</span></span>

<span data-ttu-id="ce531-136">Quando le applicazioni sono necessarie per supportare sia Windows NT che Windows 95, Windows 98 e Windows me, è utile compilare lo stesso codice per le stringhe ANSI o Unicode, a seconda della piattaforma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ce531-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="ce531-137">A questo scopo, il Windows SDK fornisce macro che mappano le stringhe a Unicode o ANSI, a seconda della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ce531-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="ce531-138">Macro</span><span class="sxs-lookup"><span data-stu-id="ce531-138">Macro</span></span>     | <span data-ttu-id="ce531-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="ce531-139">Unicode</span></span>   | <span data-ttu-id="ce531-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="ce531-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="ce531-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="ce531-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="ce531-142">TESTO ("x")</span><span class="sxs-lookup"><span data-stu-id="ce531-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="ce531-143">Ad esempio, il seguente codice:</span><span class="sxs-lookup"><span data-stu-id="ce531-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="ce531-144">viene risolto in uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="ce531-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="ce531-145">Attualmente le macro **Text** e **TCHAR** sono meno utili, perché tutte le applicazioni devono utilizzare Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce531-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="ce531-146">Tuttavia, è possibile visualizzarli nel codice precedente e in alcuni degli esempi di codice MSDN.</span><span class="sxs-lookup"><span data-stu-id="ce531-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="ce531-147">Le intestazioni per le librerie di runtime di Microsoft C definiscono un set di macro simile.</span><span class="sxs-lookup"><span data-stu-id="ce531-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="ce531-148">Ad esempio, **\_ tcslen** si risolve in **strlen** se `_UNICODE` non è definito; in caso contrario, viene risolto in **wcslen**, che è la versione a caratteri wide di **strlen**.</span><span class="sxs-lookup"><span data-stu-id="ce531-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="ce531-149">Prestare attenzione: alcune intestazioni usano il simbolo del preprocessore `UNICODE` , altre usano `_UNICODE` con un prefisso di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="ce531-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="ce531-150">Definire sempre entrambi i simboli.</span><span class="sxs-lookup"><span data-stu-id="ce531-150">Always define both symbols.</span></span> <span data-ttu-id="ce531-151">Per impostazione predefinita, Visual C++ li imposta entrambi quando si crea un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="ce531-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="ce531-152">Prossima</span><span class="sxs-lookup"><span data-stu-id="ce531-152">Next</span></span>

[<span data-ttu-id="ce531-153">Che cos'è una finestra?</span><span class="sxs-lookup"><span data-stu-id="ce531-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
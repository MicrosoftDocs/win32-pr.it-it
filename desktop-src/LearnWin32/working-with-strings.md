---
title: Uso delle stringhe
description: Uso delle stringhe
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110969"
---
# <a name="working-with-strings"></a><span data-ttu-id="6e0db-103">Uso delle stringhe</span><span class="sxs-lookup"><span data-stu-id="6e0db-103">Working with Strings</span></span>

<span data-ttu-id="6e0db-104">Windows supporta in modo nativo stringhe Unicode per elementi dell'interfaccia utente, nomi di file e così via.</span><span class="sxs-lookup"><span data-stu-id="6e0db-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="6e0db-105">Unicode è la codifica dei caratteri preferita, perché supporta tutti i set di caratteri e le lingue.</span><span class="sxs-lookup"><span data-stu-id="6e0db-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="6e0db-106">Windows rappresenta i caratteri Unicode usando la codifica UTF-16, in cui ogni carattere viene codificato come valore a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6e0db-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="6e0db-107">I caratteri UTF-16 sono detti *caratteri wide,* per distinguerli dai caratteri ANSI a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="6e0db-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="6e0db-108">Il Visual C++ supporta il tipo di dati **predefinito wchar \_ t** per i caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="6e0db-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="6e0db-109">Il file di intestazione WinNT.h definisce anche il **typedef seguente.**</span><span class="sxs-lookup"><span data-stu-id="6e0db-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="6e0db-110">Entrambe le versioni saranno disponibili nel codice di esempio MSDN.</span><span class="sxs-lookup"><span data-stu-id="6e0db-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="6e0db-111">Per dichiarare un valore letterale carattere wide o un valore letterale stringa di caratteri wide, inserire **L** prima del valore letterale.</span><span class="sxs-lookup"><span data-stu-id="6e0db-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="6e0db-112">Di seguito sono riportati altri typedef correlati alle stringhe che verranno visualizzati:</span><span class="sxs-lookup"><span data-stu-id="6e0db-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="6e0db-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="6e0db-113">Typedef</span></span>                   | <span data-ttu-id="6e0db-114">Definizione</span><span class="sxs-lookup"><span data-stu-id="6e0db-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="6e0db-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="6e0db-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="6e0db-116">**PSTR** o **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="6e0db-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="6e0db-117">**PCSTR** o **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="6e0db-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="6e0db-118">**PWSTR** o **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="6e0db-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="6e0db-119">**PCWSTR** o **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6e0db-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="6e0db-120">Funzioni Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6e0db-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="6e0db-121">Quando Microsoft ha introdotto il supporto Unicode per Windows, ha semplificato la transizione fornendo due set paralleli di API, uno per le stringhe ANSI e l'altro per le stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="6e0db-122">Ad esempio, sono disponibili due funzioni per impostare il testo della barra del titolo di una finestra:</span><span class="sxs-lookup"><span data-stu-id="6e0db-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="6e0db-123">**SetWindowTextA accetta** una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="6e0db-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="6e0db-124">**SetWindowTextW** accetta una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="6e0db-125">Internamente, la versione ANSI converte la stringa in Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="6e0db-126">Le intestazioni di Windows definiscono anche una macro che viene risolta nella versione Unicode quando viene definito il simbolo del preprocessore o la `UNICODE` versione ANSI in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e0db-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="6e0db-127">In MSDN la funzione è documentata con il nome [**SetWindowText,**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)anche se è effettivamente il nome della macro, non il nome effettivo della funzione.</span><span class="sxs-lookup"><span data-stu-id="6e0db-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="6e0db-128">Le nuove applicazioni devono sempre chiamare le versioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="6e0db-129">Molte lingue del mondo richiedono Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-129">Many world languages require Unicode.</span></span> <span data-ttu-id="6e0db-130">Se si usano stringhe ANSI, non sarà possibile localizzare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e0db-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="6e0db-131">Anche le versioni ANSI sono meno efficienti, perché il sistema operativo deve convertire le stringhe ANSI in Unicode in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6e0db-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="6e0db-132">A seconda delle preferenze, è possibile chiamare le funzioni Unicode in modo esplicito, ad esempio **SetWindowTextW,** o usare le macro.</span><span class="sxs-lookup"><span data-stu-id="6e0db-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="6e0db-133">Il codice di esempio in MSDN chiama in genere le macro, ma i due moduli sono esattamente equivalenti.</span><span class="sxs-lookup"><span data-stu-id="6e0db-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="6e0db-134">La maggior parte delle API più nuove in Windows ha solo una versione Unicode, senza una versione ANSI corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6e0db-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="6e0db-135">TCHAR</span><span class="sxs-lookup"><span data-stu-id="6e0db-135">TCHARs</span></span>

<span data-ttu-id="6e0db-136">Quando le applicazioni dovevano supportare sia Windows NT che Windows 95, Windows 98 e Windows Me, era utile compilare lo stesso codice per stringhe ANSI o Unicode, a seconda della piattaforma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6e0db-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="6e0db-137">A questo scopo, il Windows SDK macro che eseere il mapping delle stringhe a Unicode o ANSI, a seconda della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="6e0db-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="6e0db-138">Macro</span><span class="sxs-lookup"><span data-stu-id="6e0db-138">Macro</span></span>     | <span data-ttu-id="6e0db-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e0db-139">Unicode</span></span>   | <span data-ttu-id="6e0db-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="6e0db-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="6e0db-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="6e0db-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="6e0db-142">TEXT("x")</span><span class="sxs-lookup"><span data-stu-id="6e0db-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="6e0db-143">Ad esempio, il seguente codice:</span><span class="sxs-lookup"><span data-stu-id="6e0db-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="6e0db-144">viene risolto in uno degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e0db-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="6e0db-145">Le **macro TEXT** e **TCHAR** sono attualmente meno utili, perché tutte le applicazioni devono usare Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e0db-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="6e0db-146">Tuttavia, potrebbero essere visualizzati nel codice precedente e in alcuni esempi di codice MSDN.</span><span class="sxs-lookup"><span data-stu-id="6e0db-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="6e0db-147">Le intestazioni per le librerie di runtime di Microsoft C definiscono un set simile di macro.</span><span class="sxs-lookup"><span data-stu-id="6e0db-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="6e0db-148">Ad esempio, **\_ tcslen** viene risolto in **strlen** se non è definito; in caso contrario, viene risolto in wcslen , che è la versione a caratteri wide `_UNICODE` di **strlen**. </span><span class="sxs-lookup"><span data-stu-id="6e0db-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="6e0db-149">Prestare attenzione: alcune intestazioni usano il simbolo del preprocessore `UNICODE` , altre usano con un prefisso di `_UNICODE` sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="6e0db-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="6e0db-150">Definire sempre entrambi i simboli.</span><span class="sxs-lookup"><span data-stu-id="6e0db-150">Always define both symbols.</span></span> <span data-ttu-id="6e0db-151">Visual C++ vengono impostate entrambe per impostazione predefinita quando si crea un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="6e0db-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="6e0db-152">Prossima</span><span class="sxs-lookup"><span data-stu-id="6e0db-152">Next</span></span>

[<span data-ttu-id="6e0db-153">Che cos'è una finestra?</span><span class="sxs-lookup"><span data-stu-id="6e0db-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 

---
title: Regole per l'utilizzo di puntatori
description: Il porting del codice per la compilazione sia per Microsoft Windows a 32 che a 64 bit è molto semplice. È necessario seguire solo alcune semplici regole per il cast dei puntatori e usare i nuovi tipi di dati nel codice. Di seguito sono riportate le regole per la manipolazione dei puntatori.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- regole per l'utilizzo di puntatori programmazione Windows a 64 bit
- manipolazione del puntatore programmazione Windows a 64 bit
- puntatori di cast a 64 bit programmazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963527"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="f15cd-108">Regole per l'utilizzo di puntatori</span><span class="sxs-lookup"><span data-stu-id="f15cd-108">Rules for Using Pointers</span></span>

<span data-ttu-id="f15cd-109">Il porting del codice per la compilazione sia per Microsoft Windows a 32 che a 64 bit è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="f15cd-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="f15cd-110">È necessario seguire solo alcune semplici regole per il cast dei puntatori e usare i nuovi tipi di dati nel codice.</span><span class="sxs-lookup"><span data-stu-id="f15cd-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="f15cd-111">Di seguito sono riportate le regole per la manipolazione dei puntatori.</span><span class="sxs-lookup"><span data-stu-id="f15cd-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="f15cd-112">Non eseguire il cast di puntatori a **int**, **Long**, **ULONG** o **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f15cd-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="f15cd-113">Se è necessario eseguire il cast di un puntatore per testare alcuni bit, impostare o deselezionare bits oppure modificare il contenuto, utilizzare il tipo **uint \_ ptr** o **int \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="f15cd-114">Questi tipi sono tipi integrali che si adattano alle dimensioni di un puntatore per Windows a 32 e 64 bit (ad esempio, **ULONG** per windows a 32 bit e \_ Int64 per Windows a 64 bit).</span><span class="sxs-lookup"><span data-stu-id="f15cd-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="f15cd-115">Si supponga, ad esempio, di dover trasferire il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="f15cd-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="f15cd-116">Come parte del processo di porting, modificare il codice nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f15cd-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="f15cd-117">Usare **uint \_ ptr** e **int \_ ptr** laddove appropriato (e se non si è certi che siano necessari, non vi è alcun danno per usarli solo nel caso).</span><span class="sxs-lookup"><span data-stu-id="f15cd-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="f15cd-118">Non eseguire il cast dei puntatori ai tipi **ULONG**, **Long**, **int**, **uint** o **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f15cd-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="f15cd-119">Si noti che **handle** è definito come **void \***, quindi typecasting un valore di **handle** a un valore **ULONG** per testare, impostare o deselezionare i 2 bit di ordine inferiore è un errore in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="f15cd-120">Utilizzare la funzione **PtrToLong** o **PtrToUlong** per troncare i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f15cd-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="f15cd-121">Se è necessario troncare un puntatore a un valore a 32 bit, utilizzare la funzione **PtrToLong** o **PtrToUlong** (definita in Basetsd. h).</span><span class="sxs-lookup"><span data-stu-id="f15cd-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="f15cd-122">Queste funzioni disabilitano l'avviso di troncamento del puntatore per la durata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f15cd-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="f15cd-123">Usare queste funzioni con cautela.</span><span class="sxs-lookup"><span data-stu-id="f15cd-123">Use these functions carefully.</span></span> <span data-ttu-id="f15cd-124">Dopo aver convertito una variabile puntatore usando una di queste funzioni, non usarla mai come puntatore.</span><span class="sxs-lookup"><span data-stu-id="f15cd-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="f15cd-125">Queste funzioni troncano i bit 32 superiori di un indirizzo, che in genere sono necessari per accedere alla memoria a cui fa riferimento originariamente il puntatore.</span><span class="sxs-lookup"><span data-stu-id="f15cd-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="f15cd-126">L'uso di queste funzioni senza un'attenta considerazione produrrà un codice fragile.</span><span class="sxs-lookup"><span data-stu-id="f15cd-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="f15cd-127">Prestare attenzione quando si usano \_ i valori del puntatore 32 nel codice che può essere compilato come codice a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="f15cd-128">Il compilatore estenderà il puntatore quando verrà assegnato a un puntatore nativo nel codice a 64 bit, senza estendere il puntatore a zero.</span><span class="sxs-lookup"><span data-stu-id="f15cd-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="f15cd-129">Prestare attenzione quando si usano \_ i valori del puntatore 64 nel codice che può essere compilato come codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="f15cd-130">Il compilatore estenderà il puntatore nel codice a 32 bit, senza estendere il puntatore.</span><span class="sxs-lookup"><span data-stu-id="f15cd-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="f15cd-131">Prestare attenzione usando i parametri OUT.</span><span class="sxs-lookup"><span data-stu-id="f15cd-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="f15cd-132">Si supponga, ad esempio, di avere una funzione definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f15cd-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="f15cd-133">Non chiamare questa funzione come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f15cd-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="f15cd-134">Usare invece la chiamata seguente.</span><span class="sxs-lookup"><span data-stu-id="f15cd-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="f15cd-135">Typecasting &UL a **PULONG \*** impedisce un errore del compilatore, ma la funzione scriverà un valore di puntatore a 64 bit nella memoria &UL.</span><span class="sxs-lookup"><span data-stu-id="f15cd-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="f15cd-136">Questo codice funziona su Windows a 32 bit, ma provocherà il danneggiamento dei dati in Windows a 64 bit e sarà un danneggiamento difficile da trovare.</span><span class="sxs-lookup"><span data-stu-id="f15cd-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="f15cd-137">Il risultato finale è che i trucchi con il codice C non sono semplici, ma è preferibile.</span><span class="sxs-lookup"><span data-stu-id="f15cd-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="f15cd-138">Prestare attenzione alle interfacce polimorfiche.</span><span class="sxs-lookup"><span data-stu-id="f15cd-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="f15cd-139">Non creare funzioni che accettano parametri **DWORD** per i dati polimorfici.</span><span class="sxs-lookup"><span data-stu-id="f15cd-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="f15cd-140">Se i dati possono essere un puntatore o un valore integrale, utilizzare il \_ tipo uint PTR o **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="f15cd-141">Ad esempio, non creare una funzione che accetta una matrice di parametri di eccezione tipizzati come valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="f15cd-142">La matrice deve essere una matrice di **valori \_ ptr DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="f15cd-143">Gli elementi della matrice possono pertanto conservare indirizzi o valori integrali a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="f15cd-144">La regola generale è che se il tipo originale è **DWORD** ed è necessario che la larghezza del puntatore venga convertita in valore **\_ ptr DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="f15cd-145">Per questo motivo sono presenti tipi di precisione puntatore corrispondenti. Se si dispone di codice che usa **DWORD**, **ULONG** o altri tipi a 32 bit in modo polimorfico (ovvero si vuole che il parametro o il membro della struttura contenga un indirizzo), usare **uint \_ ptr** al posto del tipo corrente.</span><span class="sxs-lookup"><span data-stu-id="f15cd-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="f15cd-146">Utilizzare le nuove funzioni della classe di finestra.</span><span class="sxs-lookup"><span data-stu-id="f15cd-146">Use the new window class functions.</span></span>

    <span data-ttu-id="f15cd-147">Se si dispone di dati privati di finestra o di classe che contengono puntatori, il codice dovrà usare le nuove funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f15cd-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="f15cd-148">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="f15cd-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="f15cd-149">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="f15cd-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="f15cd-150">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="f15cd-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="f15cd-151">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="f15cd-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="f15cd-152">Queste funzioni possono essere usate in Windows a 32 e 64 bit, ma sono necessarie nelle finestre a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="f15cd-153">Preparare la transizione usando ora queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="f15cd-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="f15cd-154">Inoltre, è necessario accedere a puntatori o handle in dati privati della classe usando le nuove funzioni in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="f15cd-155">Per facilitare la ricerca di questi casi, gli indici seguenti non sono definiti in winuser. h durante una compilazione a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="f15cd-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="f15cd-156">GWL \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="f15cd-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="f15cd-157">\_HINSTANCE GWL</span><span class="sxs-lookup"><span data-stu-id="f15cd-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="f15cd-158">\_HWDPARENT GWL</span><span class="sxs-lookup"><span data-stu-id="f15cd-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="f15cd-159">\_UserData GWL</span><span class="sxs-lookup"><span data-stu-id="f15cd-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="f15cd-160">Al contrario, winuser. h definisce i nuovi indici seguenti:</span><span class="sxs-lookup"><span data-stu-id="f15cd-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="f15cd-161">GWLP \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="f15cd-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="f15cd-162">\_HINSTANCE GWLP</span><span class="sxs-lookup"><span data-stu-id="f15cd-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="f15cd-163">\_HWNDPARENT GWLP</span><span class="sxs-lookup"><span data-stu-id="f15cd-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="f15cd-164">\_UserData GWLP</span><span class="sxs-lookup"><span data-stu-id="f15cd-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="f15cd-165">\_ID GWLP</span><span class="sxs-lookup"><span data-stu-id="f15cd-165">GWLP\_ID</span></span>

    <span data-ttu-id="f15cd-166">Ad esempio, il codice seguente non viene compilato:</span><span class="sxs-lookup"><span data-stu-id="f15cd-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="f15cd-167">Deve essere modificato come segue:</span><span class="sxs-lookup"><span data-stu-id="f15cd-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="f15cd-168">Quando si imposta il membro **cbWndExtra** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , assicurarsi di riservare spazio sufficiente per i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f15cd-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="f15cd-169">Se, ad esempio, si stanno attualmente conservando i byte sizeof (DWORD) per un valore di puntatore, riservare i byte sizeof (DWORD \_ ptr).</span><span class="sxs-lookup"><span data-stu-id="f15cd-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="f15cd-170">Accedere a tutti i dati della finestra e della classe usando l' **\_ offset del campo**.</span><span class="sxs-lookup"><span data-stu-id="f15cd-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="f15cd-171">È frequente accedere ai dati della finestra usando offset hardcoded.</span><span class="sxs-lookup"><span data-stu-id="f15cd-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="f15cd-172">Questa tecnica non è portabile in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f15cd-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="f15cd-173">Per rendere portabile il codice, accedere ai dati della finestra e della classe usando la macro **\_ offset campo** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="f15cd-174">Non presupporre che il secondo puntatore abbia un offset pari a 4.</span><span class="sxs-lookup"><span data-stu-id="f15cd-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="f15cd-175">I tipi **lParam**, **wParam** e **LRESULT** cambiano dimensione con la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f15cd-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="f15cd-176">Quando si compila codice a 64 bit, questi tipi si espandono fino a 64 bit, perché in genere contengono puntatori o tipi integrali.</span><span class="sxs-lookup"><span data-stu-id="f15cd-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="f15cd-177">Non combinare questi valori con valori **DWORD**, **ULONG**, **uint**, **int**, **int** o **Long** .</span><span class="sxs-lookup"><span data-stu-id="f15cd-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="f15cd-178">Esaminare la modalità di utilizzo di questi tipi e assicurarsi di non troncare inavvertitamente i valori.</span><span class="sxs-lookup"><span data-stu-id="f15cd-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 
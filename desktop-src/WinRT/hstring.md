---
description: Handle per una stringa Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (HSTRING. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307081"
---
# <a name="hstring"></a><span data-ttu-id="1c528-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="1c528-103">HSTRING</span></span>

<span data-ttu-id="1c528-104">Handle per una stringa Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="1c528-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="1c528-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c528-105">Remarks</span></span>

<span data-ttu-id="1c528-106">Usare **HString** per rappresentare stringhe non modificabili nel Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="1c528-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="1c528-107">JavaScript e altri linguaggi, ad esempio C \# e Microsoft Visual Basic, possono usare stringhe rappresentate tramite **HString**.</span><span class="sxs-lookup"><span data-stu-id="1c528-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="1c528-108">Nella tabella seguente viene illustrato il modo in cui un **HString** viene rappresentato in altre lingue.</span><span class="sxs-lookup"><span data-stu-id="1c528-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="1c528-109">Linguaggio di programmazione</span><span class="sxs-lookup"><span data-stu-id="1c528-109">Programming Language</span></span>                                                                    | <span data-ttu-id="1c528-110">Rappresentazione di stringa</span><span class="sxs-lookup"><span data-stu-id="1c528-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="1c528-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="1c528-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="1c528-112">classe [WinRT:: HString](/uwp/cpp-ref-for-winrt/hstring)</span><span class="sxs-lookup"><span data-stu-id="1c528-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="1c528-113">Estensioni del componente Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span><span class="sxs-lookup"><span data-stu-id="1c528-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="1c528-114">Classe [Platform:: String](/cpp/cppcx/platform-string-class)</span><span class="sxs-lookup"><span data-stu-id="1c528-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="1c528-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1c528-115">JavaScript</span></span>                                                                              | <span data-ttu-id="1c528-116">String (oggetto)</span><span class="sxs-lookup"><span data-stu-id="1c528-116">String object</span></span>                                              |
| <span data-ttu-id="1c528-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="1c528-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="1c528-118">Classe System. String</span><span class="sxs-lookup"><span data-stu-id="1c528-118">System.String class</span></span>                                        |



 

<span data-ttu-id="1c528-119">L'handle **HString** è un tipo di handle standard.</span><span class="sxs-lookup"><span data-stu-id="1c528-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="1c528-120">Semanticamente, un **HString** contenente il valore **null** rappresenta la stringa vuota, costituita da caratteri di contenuto zero e da un carattere **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="1c528-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="1c528-121">La creazione di una stringa tramite [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con zero caratteri produrrà il valore dell'handle **null**.</span><span class="sxs-lookup"><span data-stu-id="1c528-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="1c528-122">Quando si chiama [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con il valore **null**, viene restituito un puntatore a una stringa vuota seguita solo dal carattere di terminazione **NUL** .</span><span class="sxs-lookup"><span data-stu-id="1c528-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="1c528-123">Non esiste alcun valore distinct per rappresentare un **HString** non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="1c528-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="1c528-124">Chiamare la funzione [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) per creare un nuovo **HString** e chiamare la funzione [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) per rilasciare il riferimento alla memoria della stringa di supporto.</span><span class="sxs-lookup"><span data-stu-id="1c528-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="1c528-125">Chiamare la funzione [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) per creare un riferimento a una stringa, anch ' esso denominato *stringa con passaggio rapido*.</span><span class="sxs-lookup"><span data-stu-id="1c528-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="1c528-126">Copiare un **HString** chiamando la funzione [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .</span><span class="sxs-lookup"><span data-stu-id="1c528-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="1c528-127">Concatenare due stringhe chiamando la funzione [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .</span><span class="sxs-lookup"><span data-stu-id="1c528-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="1c528-128">Accedere alla memoria della stringa di supporto chiamando la funzione [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .</span><span class="sxs-lookup"><span data-stu-id="1c528-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="1c528-129">**HString** può archiviare e usare caratteri **NUL** incorporati.</span><span class="sxs-lookup"><span data-stu-id="1c528-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="1c528-130">Utilizzare la funzione [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) per verificare la presenza di caratteri **NUL** incorporati prima di utilizzare qualsiasi funzione che può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="1c528-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="1c528-131">La maggior parte delle funzioni di Windows, ad esempio, utilizza **LPCWSTR** come parametro di input e calcola la lunghezza della stringa solo fino a quando non viene rilevato il primo **NUL** .</span><span class="sxs-lookup"><span data-stu-id="1c528-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="1c528-132">La stringa di supporto deve rimanere non modificabile e con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="1c528-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="1c528-133">Quando si chiama il codice crea un riferimento a una stringa tramite la funzione [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , la memoria contenente la rappresentazione di stringa di supporto è di proprietà del chiamante.</span><span class="sxs-lookup"><span data-stu-id="1c528-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="1c528-134">Il Windows Runtime si basa sul contenuto della stringa originale per rimanere invariato.</span><span class="sxs-lookup"><span data-stu-id="1c528-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="1c528-135">Quando si passa un riferimento a una stringa nel Windows Runtime, è responsabilità del chiamante assicurarsi che il contenuto della stringa sia invariato e **NUL** interrotto per la durata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="1c528-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="1c528-136">Il Windows Runtime rilascia tutti i riferimenti al riferimento alla stringa quando la chiamata restituisce.</span><span class="sxs-lookup"><span data-stu-id="1c528-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="1c528-137">Quando si riceve un **HString** come parametro out, è consigliabile impostare l'handle su **null** al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1c528-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="1c528-138">Chiamare la funzione [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per allocare un buffer di stringa modificabile che è possibile usare per creare un **HString** non modificabile.</span><span class="sxs-lookup"><span data-stu-id="1c528-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="1c528-139">Una volta completato il popolamento del buffer, chiamare la funzione [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) per creare il **HString**.</span><span class="sxs-lookup"><span data-stu-id="1c528-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="1c528-140">Questo modello di costruzione a due fasi Abilita funzionalità simili a "generatore di stringhe".</span><span class="sxs-lookup"><span data-stu-id="1c528-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="1c528-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c528-141">Requirements</span></span>



| <span data-ttu-id="1c528-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c528-142">Requirement</span></span> | <span data-ttu-id="1c528-143">Valore</span><span class="sxs-lookup"><span data-stu-id="1c528-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c528-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c528-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1c528-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c528-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="1c528-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c528-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1c528-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c528-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="1c528-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c528-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c528-149"><dt>HSTRING. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c528-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c528-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c528-150">See also</span></span>

<dl> <span data-ttu-id="1c528-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1c528-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1c528-152">**WindowsCreateString**</span><span class="sxs-lookup"><span data-stu-id="1c528-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="1c528-153">**WindowsDeleteString**</span><span class="sxs-lookup"><span data-stu-id="1c528-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="1c528-154">**WindowsDuplicateString**</span><span class="sxs-lookup"><span data-stu-id="1c528-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="1c528-155">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="1c528-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 

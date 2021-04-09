---
title: Risorsa un'STRINGTABLE
description: Definisce una o più risorse di stringa per un'applicazione. Le risorse di tipo stringa sono semplicemente stringhe Unicode o ASCII con terminazione null che possono essere caricate quando necessario dal file eseguibile, usando la funzione LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menu risorse un'STRINGTABLE e altre risorse
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117738"
---
# <a name="stringtable-resource"></a><span data-ttu-id="90bb7-105">Risorsa un'STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="90bb7-105">STRINGTABLE resource</span></span>

<span data-ttu-id="90bb7-106">Definisce una o più risorse di stringa per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="90bb7-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="90bb7-107">Le risorse di tipo stringa sono semplicemente stringhe Unicode o ASCII con terminazione null che possono essere caricate quando necessario dal file eseguibile, usando la funzione [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .</span><span class="sxs-lookup"><span data-stu-id="90bb7-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="90bb7-108">Esistono due modi per formattare un'istruzione **un'STRINGTABLE** :</span><span class="sxs-lookup"><span data-stu-id="90bb7-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="90bb7-109">\- - oppure -</span><span class="sxs-lookup"><span data-stu-id="90bb7-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="90bb7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="90bb7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90bb7-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="90bb7-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="90bb7-112">Questo parametro può essere costituito da zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="90bb7-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="90bb7-113">Istruzione</span><span class="sxs-lookup"><span data-stu-id="90bb7-113">Statement</span></span>                                                        | <span data-ttu-id="90bb7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90bb7-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90bb7-115">[**Caratteristiche**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="90bb7-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="90bb7-116">Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse.</span><span class="sxs-lookup"><span data-stu-id="90bb7-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="90bb7-117">Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90bb7-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="90bb7-118">[](language-statement.md) *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="90bb7-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="90bb7-119">Specifica la lingua per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="90bb7-119">Specifies the language for the resource.</span></span> <span data-ttu-id="90bb7-120">Per ulteriori informazioni, vedere [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90bb7-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="90bb7-121">[](version-statement.md) *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="90bb7-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="90bb7-122">Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse.</span><span class="sxs-lookup"><span data-stu-id="90bb7-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="90bb7-123">Per ulteriori informazioni, vedere [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="90bb7-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="90bb7-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="90bb7-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="90bb7-125">Intero senza segno a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="90bb7-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="90bb7-126"><span id="string"></span><span id="STRING"></span>*stringa*</span><span class="sxs-lookup"><span data-stu-id="90bb7-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="90bb7-127">Una o più stringhe, racchiuse tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="90bb7-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="90bb7-128">La stringa non deve contenere più di 4097 caratteri e deve occupare una sola riga nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="90bb7-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="90bb7-129">Per aggiungere un ritorno a capo alla stringa, usare questa sequenza di caratteri: \\ 012.</span><span class="sxs-lookup"><span data-stu-id="90bb7-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="90bb7-130">Ad esempio, "Line One \\ 012Line Two" definisce una stringa che viene visualizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="90bb7-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="90bb7-131">Per incorporare le virgolette nella stringa, usare la sequenza seguente: "".</span><span class="sxs-lookup"><span data-stu-id="90bb7-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="90bb7-132">Ad esempio, "" "riga tre" "" definisce una stringa che viene visualizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="90bb7-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="90bb7-133">Per codificare i caratteri Unicode, usare "L" seguito dai caratteri Unicode racchiusi tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="90bb7-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="90bb7-134">Per un esempio, vedere la sezione esempi.</span><span class="sxs-lookup"><span data-stu-id="90bb7-134">See the Examples section for an example.</span></span>

<span data-ttu-id="90bb7-135">Il compilatore di risorse supporta inoltre le continuazioni di riga nella *stringa*.</span><span class="sxs-lookup"><span data-stu-id="90bb7-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="90bb7-136">Per un esempio, vedere la sezione esempi.</span><span class="sxs-lookup"><span data-stu-id="90bb7-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="90bb7-137">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="90bb7-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="90bb7-138">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="90bb7-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90bb7-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="90bb7-139">Remarks</span></span>

<span data-ttu-id="90bb7-140">RC alloca 16 stringhe per sezione e usa il valore Identifier per determinare quale sezione deve contenere la stringa.</span><span class="sxs-lookup"><span data-stu-id="90bb7-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="90bb7-141">Le stringhe i cui identificatori differiscono solo nei 4 bit inferiori vengono inserite nella stessa sezione.</span><span class="sxs-lookup"><span data-stu-id="90bb7-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="90bb7-142">Per ulteriori informazioni, vedere [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="90bb7-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="90bb7-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="90bb7-143">Examples</span></span>

<span data-ttu-id="90bb7-144">Nell'esempio seguente viene illustrato l'uso dell'istruzione **un'STRINGTABLE** per visualizzare le stringhe ASCII:</span><span class="sxs-lookup"><span data-stu-id="90bb7-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="90bb7-145">Nell'esempio seguente viene illustrato come codificare i caratteri Unicode:</span><span class="sxs-lookup"><span data-stu-id="90bb7-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="90bb7-146">Nell'esempio seguente vengono illustrate le stringhe con ASCII e Unicode.</span><span class="sxs-lookup"><span data-stu-id="90bb7-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="90bb7-147">Si noti che le stringhe senza "L" iniziale utilizzano il formato di escape a 2 cifre:</span><span class="sxs-lookup"><span data-stu-id="90bb7-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="90bb7-148">Nell'esempio seguente viene illustrato come è possibile utilizzare le continuazioni di riga:</span><span class="sxs-lookup"><span data-stu-id="90bb7-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="90bb7-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90bb7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bb7-150">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="90bb7-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="90bb7-151">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="90bb7-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="90bb7-152">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="90bb7-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="90bb7-153">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="90bb7-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="90bb7-154">**MENU**</span><span class="sxs-lookup"><span data-stu-id="90bb7-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="90bb7-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="90bb7-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="90bb7-156">**Versione**</span><span class="sxs-lookup"><span data-stu-id="90bb7-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
---
title: Risorsa RCDATA
description: Definisce una risorsa di dati non elaborati per un'applicazione. Le risorse dei dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menu risorse RCDATA e altre risorse
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956004"
---
# <a name="rcdata-resource"></a><span data-ttu-id="820c3-105">Risorsa RCDATA</span><span class="sxs-lookup"><span data-stu-id="820c3-105">RCDATA resource</span></span>

<span data-ttu-id="820c3-106">Definisce una risorsa di dati non elaborati per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="820c3-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="820c3-107">Le risorse dei dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="820c3-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="820c3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="820c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820c3-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="820c3-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="820c3-110">Nome univoco o valore Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="820c3-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="820c3-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="820c3-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="820c3-112">Questo parametro può essere costituito da zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="820c3-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="820c3-113">Istruzione</span><span class="sxs-lookup"><span data-stu-id="820c3-113">Statement</span></span>                                                        | <span data-ttu-id="820c3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="820c3-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="820c3-115">[**Caratteristiche**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="820c3-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="820c3-116">Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse.</span><span class="sxs-lookup"><span data-stu-id="820c3-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="820c3-117">Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="820c3-118">[](language-statement.md) *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="820c3-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="820c3-119">Lingua per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="820c3-119">Language for the resource.</span></span> <span data-ttu-id="820c3-120">Per ulteriori informazioni, vedere [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="820c3-121">[](version-statement.md) *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="820c3-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="820c3-122">Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse.</span><span class="sxs-lookup"><span data-stu-id="820c3-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="820c3-123">Per ulteriori informazioni, vedere [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="820c3-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*</span><span class="sxs-lookup"><span data-stu-id="820c3-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="820c3-125">Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="820c3-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="820c3-126">I numeri interi possono essere specificati in formato decimale, ottale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="820c3-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="820c3-127">Per essere compatibile con Windows a 16 bit, i numeri interi vengono archiviati come valori di **Word** .</span><span class="sxs-lookup"><span data-stu-id="820c3-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="820c3-128">È possibile archiviare un valore integer come valore **DWORD** qualificando l'Integer con il suffisso "L".</span><span class="sxs-lookup"><span data-stu-id="820c3-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="820c3-129">Le stringhe sono racchiuse tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="820c3-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="820c3-130">RC non aggiunge automaticamente un carattere di terminazione null a una stringa.</span><span class="sxs-lookup"><span data-stu-id="820c3-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="820c3-131">Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso L.</span><span class="sxs-lookup"><span data-stu-id="820c3-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="820c3-132">Il blocco di dati inizia in un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del blocco di *dati non elaborati* .</span><span class="sxs-lookup"><span data-stu-id="820c3-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="820c3-133">È responsabilità dell'utente assicurare l'allineamento corretto dei dati all'interno del blocco.</span><span class="sxs-lookup"><span data-stu-id="820c3-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="820c3-134">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="820c3-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="820c3-135">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="820c3-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="820c3-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="820c3-136">Examples</span></span>

<span data-ttu-id="820c3-137">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RCDATA** :</span><span class="sxs-lookup"><span data-stu-id="820c3-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="820c3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="820c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820c3-139">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="820c3-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="820c3-140">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="820c3-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="820c3-141">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="820c3-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="820c3-142">**MENU**</span><span class="sxs-lookup"><span data-stu-id="820c3-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="820c3-143">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="820c3-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="820c3-144">**Versione**</span><span class="sxs-lookup"><span data-stu-id="820c3-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 





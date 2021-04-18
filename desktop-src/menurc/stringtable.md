---
title: Struttura un'STRINGTABLE
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla formattazione della lingua e della tabella codici per le stringhe specificate dal membro figlio. Una tabella codici è un set di caratteri ordinato.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menu struttura un'STRINGTABLE e altre risorse
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400365"
---
# <a name="stringtable-structure"></a><span data-ttu-id="a593c-106">Struttura un'STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="a593c-106">StringTable structure</span></span>

<span data-ttu-id="a593c-107">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="a593c-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="a593c-108">Contiene informazioni sulla formattazione della lingua e della tabella codici per le stringhe specificate dal membro **figlio** .</span><span class="sxs-lookup"><span data-stu-id="a593c-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="a593c-109">Una tabella codici è un set di caratteri ordinato.</span><span class="sxs-lookup"><span data-stu-id="a593c-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a593c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a593c-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="a593c-111">Members</span><span class="sxs-lookup"><span data-stu-id="a593c-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="a593c-112">**wLength**</span><span class="sxs-lookup"><span data-stu-id="a593c-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-113">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="a593c-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-114">Lunghezza, in byte, della struttura **un'STRINGTABLE** , incluse tutte le strutture indicate dal membro **figlio** .</span><span class="sxs-lookup"><span data-stu-id="a593c-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="a593c-115">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="a593c-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="a593c-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-117">Questo membro è sempre uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="a593c-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a593c-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="a593c-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-119">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="a593c-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-120">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="a593c-120">The type of data in the version resource.</span></span> <span data-ttu-id="a593c-121">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="a593c-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="a593c-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="a593c-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-123">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="a593c-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-124">Numero esadecimale a 8 cifre archiviato come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="a593c-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="a593c-125">Le quattro cifre più significative rappresentano l'identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="a593c-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="a593c-126">Le quattro cifre meno significative rappresentano la tabella codici per la quale vengono formattati i dati.</span><span class="sxs-lookup"><span data-stu-id="a593c-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="a593c-127">Ogni identificatore di linguaggio standard Microsoft contiene due parti: i 10 bit di ordine inferiore specificano la lingua principale e i 6 bit più significativi specificano il linguaggio di sottolinguaggio.</span><span class="sxs-lookup"><span data-stu-id="a593c-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="a593c-128">Per una tabella di identificatori validi, vedere.</span><span class="sxs-lookup"><span data-stu-id="a593c-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="a593c-129">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="a593c-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-130">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="a593c-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-131">Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="a593c-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="a593c-132">**Children**</span><span class="sxs-lookup"><span data-stu-id="a593c-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="a593c-133">Tipo: **[ **stringa**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="a593c-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a593c-134">Matrice di una o più strutture di [**stringa**](string-str.md) .</span><span class="sxs-lookup"><span data-stu-id="a593c-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a593c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="a593c-135">Remarks</span></span>

<span data-ttu-id="a593c-136">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="a593c-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="a593c-137">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a593c-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="a593c-138">Il membro **figlio** della struttura [**StringFileInfo**](stringfileinfo.md) contiene almeno una struttura **un'STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="a593c-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="a593c-139">Impostare la parte relativa alla tabella codici del membro **szKey** sul valore esadecimale 0x04B0 per indicare la tabella codici Unicode o sul valore esadecimale della tabella codici appropriata per il componente del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="a593c-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="a593c-140">Dopo aver scelto il valore per la tabella codici, è necessario continuare a usare lo stesso valore nelle revisioni successive del file.</span><span class="sxs-lookup"><span data-stu-id="a593c-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="a593c-141">Un file eseguibile o una DLL che supporta più lingue deve avere una risorsa di versione per ogni lingua, anziché una singola risorsa di versione contenente stringhe in diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="a593c-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="a593c-142">Tuttavia, se si usa la struttura [**var**](var-str.md) per elencare le lingue supportate dall'applicazione, il numero di strutture **un'STRINGTABLE** nella risorsa Version è direttamente correlato al numero di coppie lingua/identificatore tabella codici nel membro **value** della struttura **var** .</span><span class="sxs-lookup"><span data-stu-id="a593c-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a593c-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a593c-143">Requirements</span></span>



| <span data-ttu-id="a593c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a593c-144">Requirement</span></span> | <span data-ttu-id="a593c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="a593c-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a593c-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a593c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a593c-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a593c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a593c-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a593c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a593c-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a593c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a593c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a593c-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="a593c-151">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a593c-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a593c-152">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="a593c-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="a593c-153">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="a593c-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="a593c-154">**Var**</span><span class="sxs-lookup"><span data-stu-id="a593c-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="a593c-155">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="a593c-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="a593c-156">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="a593c-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="a593c-157">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a593c-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a593c-158">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="a593c-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






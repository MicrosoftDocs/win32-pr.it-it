---
title: Struttura StringFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che possono essere visualizzate per una lingua e una tabella codici particolari.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menu struttura StringFileInfo e altre risorse
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963893"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="4567a-105">Struttura StringFileInfo</span><span class="sxs-lookup"><span data-stu-id="4567a-105">StringFileInfo structure</span></span>

<span data-ttu-id="4567a-106">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="4567a-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="4567a-107">Contiene informazioni sulla versione che possono essere visualizzate per una lingua e una tabella codici particolari.</span><span class="sxs-lookup"><span data-stu-id="4567a-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="4567a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4567a-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="4567a-109">Members</span><span class="sxs-lookup"><span data-stu-id="4567a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4567a-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="4567a-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4567a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-112">Lunghezza, in byte, dell'intero blocco **StringFileInfo** , incluse tutte le strutture indicate dal membro **figlio** .</span><span class="sxs-lookup"><span data-stu-id="4567a-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="4567a-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="4567a-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4567a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-115">Questo membro è sempre uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="4567a-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4567a-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="4567a-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4567a-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-118">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="4567a-118">The type of data in the version resource.</span></span> <span data-ttu-id="4567a-119">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="4567a-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="4567a-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="4567a-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="4567a-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-122">Stringa Unicode L "StringFileInfo".</span><span class="sxs-lookup"><span data-stu-id="4567a-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="4567a-123">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="4567a-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4567a-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-125">Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="4567a-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="4567a-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="4567a-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="4567a-127">Tipo: **[ **un'STRINGTABLE**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="4567a-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4567a-128">Matrice di una o più strutture [**un'STRINGTABLE**](stringtable.md) .</span><span class="sxs-lookup"><span data-stu-id="4567a-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="4567a-129">Ogni membro **szKey** della struttura **un'STRINGTABLE** indica la lingua e la tabella codici appropriate per la visualizzazione del testo nella struttura **un'STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="4567a-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4567a-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="4567a-130">Remarks</span></span>

<span data-ttu-id="4567a-131">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="4567a-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="4567a-132">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4567a-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="4567a-133">Il membro **figlio** della struttura di [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o più strutture **StringFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="4567a-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="4567a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4567a-134">Requirements</span></span>



| <span data-ttu-id="4567a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4567a-135">Requirement</span></span> | <span data-ttu-id="4567a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4567a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4567a-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4567a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4567a-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4567a-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4567a-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4567a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4567a-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4567a-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4567a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4567a-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="4567a-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4567a-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4567a-143">**Un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="4567a-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="4567a-144">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="4567a-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="4567a-145">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="4567a-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="4567a-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4567a-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4567a-147">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="4567a-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






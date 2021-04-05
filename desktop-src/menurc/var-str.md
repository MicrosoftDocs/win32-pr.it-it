---
title: Struttura var
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene in genere un elenco di coppie di identificatori di tabella codici e lingue supportate dalla versione dell'applicazione o dalla DLL.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menu struttura var e altre risorse
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874526"
---
# <a name="var-structure"></a><span data-ttu-id="bdff6-105">Struttura var</span><span class="sxs-lookup"><span data-stu-id="bdff6-105">Var structure</span></span>

<span data-ttu-id="bdff6-106">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="bdff6-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="bdff6-107">Contiene in genere un elenco di coppie di identificatori di tabella codici e lingue supportate dalla versione dell'applicazione o dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="bdff6-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdff6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdff6-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="bdff6-109">Members</span><span class="sxs-lookup"><span data-stu-id="bdff6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="bdff6-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="bdff6-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bdff6-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-112">Lunghezza, in byte, della struttura **var** .</span><span class="sxs-lookup"><span data-stu-id="bdff6-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="bdff6-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bdff6-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-115">Lunghezza, in byte, del membro del **valore** .</span><span class="sxs-lookup"><span data-stu-id="bdff6-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="bdff6-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bdff6-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-118">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="bdff6-118">The type of data in the version resource.</span></span> <span data-ttu-id="bdff6-119">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="bdff6-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="bdff6-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="bdff6-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-122">Stringa Unicode L "Translation".</span><span class="sxs-lookup"><span data-stu-id="bdff6-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-123">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="bdff6-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bdff6-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-125">Il numero di parole necessarie per allineare il membro del **valore** a un limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="bdff6-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-126">**Valore**</span><span class="sxs-lookup"><span data-stu-id="bdff6-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="bdff6-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bdff6-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="bdff6-128">Matrice di uno o più valori che sono coppie di identificatori della tabella codici e della lingua.</span><span class="sxs-lookup"><span data-stu-id="bdff6-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="bdff6-129">Per ulteriori informazioni, vedere la sezione Osservazioni seguente.</span><span class="sxs-lookup"><span data-stu-id="bdff6-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdff6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdff6-130">Remarks</span></span>

<span data-ttu-id="bdff6-131">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="bdff6-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="bdff6-132">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bdff6-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="bdff6-133">Se si usa la struttura **var** per elencare le lingue supportate dall'applicazione o dalla dll invece di usare più risorse della versione, usare il membro **valore** per contenere una matrice di valori **DWORD** che indica le combinazioni di lingua e tabella codici supportate da questo file.</span><span class="sxs-lookup"><span data-stu-id="bdff6-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="bdff6-134">La parola più bassa di ogni **valore DWORD** deve contenere un identificatore di lingua Microsoft e la parola più significativa deve contenere il numero della tabella codici IBM.</span><span class="sxs-lookup"><span data-stu-id="bdff6-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="bdff6-135">La parola di ordine superiore o inferiore può essere zero, a indicare che il file è indipendente dalla lingua o dalla tabella codici.</span><span class="sxs-lookup"><span data-stu-id="bdff6-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="bdff6-136">Se la struttura **var** viene omessa, il file verrà interpretato sia come lingua sia come tabella codici indipendente.</span><span class="sxs-lookup"><span data-stu-id="bdff6-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdff6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdff6-137">Requirements</span></span>



| <span data-ttu-id="bdff6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdff6-138">Requirement</span></span> | <span data-ttu-id="bdff6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="bdff6-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bdff6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdff6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bdff6-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdff6-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bdff6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdff6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bdff6-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdff6-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bdff6-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdff6-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="bdff6-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bdff6-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdff6-146">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="bdff6-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="bdff6-147">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="bdff6-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="bdff6-148">**Un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="bdff6-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="bdff6-149">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="bdff6-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="bdff6-150">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bdff6-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bdff6-151">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="bdff6-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






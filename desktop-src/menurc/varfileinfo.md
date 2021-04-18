---
title: Struttura VarFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che non dipendono da una determinata combinazione di lingua e tabella codici.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menu struttura VarFileInfo e altre risorse
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302206"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="ef644-105">Struttura VarFileInfo</span><span class="sxs-lookup"><span data-stu-id="ef644-105">VarFileInfo structure</span></span>

<span data-ttu-id="ef644-106">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="ef644-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="ef644-107">Contiene informazioni sulla versione che non dipendono da una determinata combinazione di lingua e tabella codici.</span><span class="sxs-lookup"><span data-stu-id="ef644-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef644-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef644-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="ef644-109">Members</span><span class="sxs-lookup"><span data-stu-id="ef644-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef644-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="ef644-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ef644-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-112">Lunghezza, in byte, dell'intero blocco **VarFileInfo** , incluse tutte le strutture indicate dal membro **figlio** .</span><span class="sxs-lookup"><span data-stu-id="ef644-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="ef644-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="ef644-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ef644-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-115">Questo membro è sempre uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="ef644-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ef644-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="ef644-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ef644-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-118">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="ef644-118">The type of data in the version resource.</span></span> <span data-ttu-id="ef644-119">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="ef644-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="ef644-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="ef644-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="ef644-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-122">Stringa Unicode L "VarFileInfo".</span><span class="sxs-lookup"><span data-stu-id="ef644-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="ef644-123">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="ef644-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="ef644-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-125">Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="ef644-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="ef644-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="ef644-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="ef644-127">Tipo: **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="ef644-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef644-128">Contiene in genere un elenco di lingue supportate dall'applicazione o dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="ef644-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef644-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef644-129">Remarks</span></span>

<span data-ttu-id="ef644-130">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="ef644-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="ef644-131">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ef644-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="ef644-132">Il membro **figlio** della struttura di [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o una o più strutture **VarFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="ef644-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef644-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef644-133">Requirements</span></span>



| <span data-ttu-id="ef644-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef644-134">Requirement</span></span> | <span data-ttu-id="ef644-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ef644-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ef644-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef644-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ef644-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef644-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef644-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef644-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ef644-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef644-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ef644-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef644-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef644-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ef644-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef644-142">**Var**</span><span class="sxs-lookup"><span data-stu-id="ef644-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="ef644-143">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="ef644-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="ef644-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ef644-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef644-145">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="ef644-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






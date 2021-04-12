---
title: Struttura FONTGROUPHDR
description: Contiene le informazioni necessarie a un'applicazione per accedere a un tipo di carattere specifico. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menu struttura FONTGROUPHDR e altre risorse
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225228"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="608bb-105">Struttura FONTGROUPHDR</span><span class="sxs-lookup"><span data-stu-id="608bb-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="608bb-106">Contiene le informazioni necessarie a un'applicazione per accedere a un tipo di carattere specifico.</span><span class="sxs-lookup"><span data-stu-id="608bb-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="608bb-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="608bb-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="608bb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="608bb-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="608bb-109">Members</span><span class="sxs-lookup"><span data-stu-id="608bb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="608bb-110">**NumberOfFonts**</span><span class="sxs-lookup"><span data-stu-id="608bb-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="608bb-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="608bb-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="608bb-112">Numero di singoli tipi di carattere associati a questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="608bb-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="608bb-113">**DE**</span><span class="sxs-lookup"><span data-stu-id="608bb-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="608bb-114">Tipo: **[ **dirente**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="608bb-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="608bb-115">Struttura che contiene un identificatore ordinale univoco per ogni tipo di carattere nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="608bb-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="608bb-116">Il membro **de** è un segnaposto per la matrice a lunghezza variabile delle strutture di [**dislocazione**](direntry.md) .</span><span class="sxs-lookup"><span data-stu-id="608bb-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="608bb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="608bb-117">Remarks</span></span>

<span data-ttu-id="608bb-118">La struttura **FONTGROUPHDR** segue i dati per i singoli tipi di carattere in. File res.</span><span class="sxs-lookup"><span data-stu-id="608bb-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="608bb-119">Il compilatore di risorse aggiunge automaticamente la struttura **FONTGROUPHDR** , in genere come ultima voce nel file.</span><span class="sxs-lookup"><span data-stu-id="608bb-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="608bb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="608bb-120">Requirements</span></span>



| <span data-ttu-id="608bb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="608bb-121">Requirement</span></span> | <span data-ttu-id="608bb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="608bb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="608bb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="608bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="608bb-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="608bb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="608bb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="608bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="608bb-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="608bb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="608bb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="608bb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="608bb-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="608bb-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="608bb-129">**Diaffitto**</span><span class="sxs-lookup"><span data-stu-id="608bb-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="608bb-130">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="608bb-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="608bb-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="608bb-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="608bb-132">Risorse</span><span class="sxs-lookup"><span data-stu-id="608bb-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 






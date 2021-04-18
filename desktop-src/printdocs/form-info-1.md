---
description: La struttura FORM_INFO_1 contiene informazioni su un modulo di stampa. Le informazioni includono l'origine dei form di stampa, il nome, le dimensioni e le dimensioni dell'area stampabile.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Struttura FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314017"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="2e966-104">Struttura FORM_INFO_1</span><span class="sxs-lookup"><span data-stu-id="2e966-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="2e966-105">La struttura **FORM_INFO_1** contiene informazioni su un modulo di stampa.</span><span class="sxs-lookup"><span data-stu-id="2e966-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="2e966-106">Le informazioni includono l'origine del modulo di stampa, il nome, le dimensioni e le dimensioni dell'area stampabile.</span><span class="sxs-lookup"><span data-stu-id="2e966-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e966-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e966-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="2e966-108">Members</span><span class="sxs-lookup"><span data-stu-id="2e966-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e966-109">**Flag**</span><span class="sxs-lookup"><span data-stu-id="2e966-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2e966-110">Proprietà del form.</span><span class="sxs-lookup"><span data-stu-id="2e966-110">The form properties.</span></span> <span data-ttu-id="2e966-111">Vengono definiti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e966-111">The following values are defined.</span></span>



| <span data-ttu-id="2e966-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2e966-112">Value</span></span>         | <span data-ttu-id="2e966-113">Significato</span><span class="sxs-lookup"><span data-stu-id="2e966-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e966-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="2e966-114">FORM_USER</span></span>    | <span data-ttu-id="2e966-115">Se viene impostato questo flag di bit, il form è stato definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2e966-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="2e966-116">I form con questo set di flag sono definiti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2e966-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="2e966-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="2e966-117">FORM_BUILTIN</span></span> | <span data-ttu-id="2e966-118">Se viene impostato questo flag di bit, il form fa parte dello spooler.</span><span class="sxs-lookup"><span data-stu-id="2e966-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="2e966-119">Le definizioni dei moduli con questo set di flag non vengono visualizzate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2e966-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="2e966-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="2e966-120">FORM_PRINTER</span></span> | <span data-ttu-id="2e966-121">Se viene impostato questo flag di bit, il form è associato a una determinata stampante e la relativa definizione viene visualizzata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2e966-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="2e966-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="2e966-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="2e966-123">Puntatore a una stringa con terminazione null che specifica il nome del form.</span><span class="sxs-lookup"><span data-stu-id="2e966-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="2e966-124">Il nome del modulo non può superare i 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2e966-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="2e966-125">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="2e966-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="2e966-126">Larghezza e altezza, in millesimi di millimetri, del form.</span><span class="sxs-lookup"><span data-stu-id="2e966-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="2e966-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="2e966-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="2e966-128">Larghezza e altezza, in millesimi di millimetri, del form.</span><span class="sxs-lookup"><span data-stu-id="2e966-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e966-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e966-129">Requirements</span></span>



| <span data-ttu-id="2e966-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e966-130">Requirement</span></span> | <span data-ttu-id="2e966-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2e966-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e966-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e966-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2e966-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e966-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2e966-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e966-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2e966-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e966-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e966-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e966-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e966-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e966-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2e966-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2e966-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2e966-139">**_FORM_INFO_1W** (Unicode) e **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2e966-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="2e966-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e966-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e966-141">Stampa</span><span class="sxs-lookup"><span data-stu-id="2e966-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2e966-142">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="2e966-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2e966-143">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="2e966-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="2e966-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="2e966-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="2e966-145">**Diformi**</span><span class="sxs-lookup"><span data-stu-id="2e966-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 





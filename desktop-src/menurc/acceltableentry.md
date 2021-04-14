---
title: Struttura ACCELTABLEENTRY
description: Descrive i dati in una singola risorsa della tabella dei tasti di scelta rapida. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menu struttura ACCELTABLEENTRY e altre risorse
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479084"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="22a1c-105">Struttura ACCELTABLEENTRY</span><span class="sxs-lookup"><span data-stu-id="22a1c-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="22a1c-106">Descrive i dati in una singola risorsa della tabella dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="22a1c-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="22a1c-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="22a1c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22a1c-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="22a1c-109">Members</span><span class="sxs-lookup"><span data-stu-id="22a1c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="22a1c-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="22a1c-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="22a1c-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="22a1c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="22a1c-112">Descrive le caratteristiche del tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="22a1c-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="22a1c-113">Questo membro può avere uno o più dei seguenti valori da winuser. h.</span><span class="sxs-lookup"><span data-stu-id="22a1c-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="22a1c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="22a1c-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="22a1c-115">Significato</span><span class="sxs-lookup"><span data-stu-id="22a1c-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="22a1c-116"><dt>**FVIRTKEY**</dt> <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="22a1c-117">Il tasto di scelta rapida è un [codice a chiave virtuale](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="22a1c-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="22a1c-118">Se questo flag non viene specificato, si presuppone che il tasto di scelta rapida specifichi un codice carattere ASCII.</span><span class="sxs-lookup"><span data-stu-id="22a1c-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="22a1c-119"><dt></dt> <dt>0x02</dt> FNOINVERT</span><span class="sxs-lookup"><span data-stu-id="22a1c-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="22a1c-120">Una voce di menu sulla barra dei menu non viene evidenziata quando si utilizza un acceleratore.</span><span class="sxs-lookup"><span data-stu-id="22a1c-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="22a1c-121">Questo attributo è obsoleto e viene mantenuto solo per compatibilità con le versioni precedenti dei file di risorse progettati per Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="22a1c-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="22a1c-122"><dt></dt> <dt>0x04</dt> FSHIFT</span><span class="sxs-lookup"><span data-stu-id="22a1c-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="22a1c-123">L'acceleratore viene attivato solo se l'utente preme il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="22a1c-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="22a1c-124">Questo flag è valido solo per le chiavi virtuali.</span><span class="sxs-lookup"><span data-stu-id="22a1c-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="22a1c-125"><dt></dt> <dt>0x08</dt> FCONTROL</span><span class="sxs-lookup"><span data-stu-id="22a1c-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="22a1c-126">L'acceleratore viene attivato solo se l'utente preme il tasto CTRL.</span><span class="sxs-lookup"><span data-stu-id="22a1c-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="22a1c-127">Questo flag è valido solo per le chiavi virtuali.</span><span class="sxs-lookup"><span data-stu-id="22a1c-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="22a1c-128"><dt></dt> <dt>0x10</dt> Falt</span><span class="sxs-lookup"><span data-stu-id="22a1c-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="22a1c-129">L'acceleratore viene attivato solo se l'utente preme il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="22a1c-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="22a1c-130">Questo flag è valido solo per le chiavi virtuali.</span><span class="sxs-lookup"><span data-stu-id="22a1c-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="22a1c-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="22a1c-132">La voce è l'ultima in una tabella di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="22a1c-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="22a1c-133">**wAnsi**</span><span class="sxs-lookup"><span data-stu-id="22a1c-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="22a1c-134">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="22a1c-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="22a1c-135">Valore del carattere ANSI o codice di chiave virtuale che identifica il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="22a1c-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="22a1c-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="22a1c-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="22a1c-137">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="22a1c-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="22a1c-138">Identificatore per il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="22a1c-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="22a1c-139">Si tratta del valore passato alla routine della finestra quando l'utente preme il tasto specificato.</span><span class="sxs-lookup"><span data-stu-id="22a1c-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="22a1c-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="22a1c-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="22a1c-141">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="22a1c-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="22a1c-142">Numero di byte inseriti per garantire che la struttura sia allineata a un limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="22a1c-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22a1c-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="22a1c-143">Remarks</span></span>

<span data-ttu-id="22a1c-144">La struttura **ACCELTABLEENTRY** viene ripetuta per tutte le voci della tabella di tasti di scelta rapida nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="22a1c-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="22a1c-145">L'ultima voce nella tabella è contrassegnata con il valore 0x0080.</span><span class="sxs-lookup"><span data-stu-id="22a1c-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="22a1c-146">È possibile calcolare il numero di elementi nella tabella se si divide la lunghezza della risorsa di otto.</span><span class="sxs-lookup"><span data-stu-id="22a1c-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="22a1c-147">L'applicazione può quindi accedere in modo casuale alle singole voci a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="22a1c-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a1c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22a1c-148">Requirements</span></span>



| <span data-ttu-id="22a1c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a1c-149">Requirement</span></span> | <span data-ttu-id="22a1c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="22a1c-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="22a1c-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a1c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="22a1c-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22a1c-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22a1c-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a1c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="22a1c-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22a1c-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="22a1c-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22a1c-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="22a1c-156">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="22a1c-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22a1c-157">**CreateAcceleratorTable**</span><span class="sxs-lookup"><span data-stu-id="22a1c-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="22a1c-158">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="22a1c-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22a1c-159">Risorse</span><span class="sxs-lookup"><span data-stu-id="22a1c-159">Resources</span></span>](resources.md)
</dt> </dl>

 


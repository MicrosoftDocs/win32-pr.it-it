---
description: La struttura della porta \_ info \_ 3 specifica il valore di stato di una porta stampante.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Struttura PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311813"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="c3cce-103">Struttura delle informazioni sulla porta \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="c3cce-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="c3cce-104">La struttura della **porta \_ info \_ 3** specifica il valore di stato di una porta stampante.</span><span class="sxs-lookup"><span data-stu-id="c3cce-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3cce-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="c3cce-106">Members</span><span class="sxs-lookup"><span data-stu-id="c3cce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3cce-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="c3cce-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c3cce-108">Nuovo valore dello stato della porta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-108">The new port status value.</span></span> <span data-ttu-id="c3cce-109">Questo valore viene utilizzato solo se il membro **pszStatus** è **null**.</span><span class="sxs-lookup"><span data-stu-id="c3cce-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="c3cce-110">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3cce-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="c3cce-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c3cce-111">Value</span></span>                            | <span data-ttu-id="c3cce-112">Significato</span><span class="sxs-lookup"><span data-stu-id="c3cce-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c3cce-113">0</span><span class="sxs-lookup"><span data-stu-id="c3cce-113">0</span></span>                                | <span data-ttu-id="c3cce-114">Cancella lo stato della porta stampante.</span><span class="sxs-lookup"><span data-stu-id="c3cce-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="c3cce-115">\_stato porta \_ offline</span><span class="sxs-lookup"><span data-stu-id="c3cce-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="c3cce-116">La stampante della porta è offline.</span><span class="sxs-lookup"><span data-stu-id="c3cce-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="c3cce-117">\_ \_ inceppamento carta stato porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="c3cce-118">Alla stampante della porta è associato un inceppamento della carta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="c3cce-119">carta di stato porta in \_ \_ \_ uscita</span><span class="sxs-lookup"><span data-stu-id="c3cce-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="c3cce-120">La stampante della porta è fuori carta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="c3cce-121">\_ \_ bin output stato \_ porta \_ completo</span><span class="sxs-lookup"><span data-stu-id="c3cce-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="c3cce-122">Il contenitore di output printer's della porta è pieno.</span><span class="sxs-lookup"><span data-stu-id="c3cce-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="c3cce-123">problema relativo alla carta di stato della porta \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="c3cce-124">La stampante della porta presenta un problema relativo alla carta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="c3cce-125">\_stato porta \_ senza \_ toner</span><span class="sxs-lookup"><span data-stu-id="c3cce-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="c3cce-126">La stampante della porta non è presente nel toner.</span><span class="sxs-lookup"><span data-stu-id="c3cce-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="c3cce-127">\_sportello stato \_ porta \_ aperto</span><span class="sxs-lookup"><span data-stu-id="c3cce-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="c3cce-128">La porta della stampante della porta è aperta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="c3cce-129">\_ \_ intervento dell'utente stato porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="c3cce-130">La stampante della porta richiede l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c3cce-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="c3cce-131">\_ \_ \_ memoria insufficiente per lo stato della porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="c3cce-132">La stampante della porta ha esaurito la memoria.</span><span class="sxs-lookup"><span data-stu-id="c3cce-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="c3cce-133">\_ \_ toner stato porta \_ basso</span><span class="sxs-lookup"><span data-stu-id="c3cce-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="c3cce-134">Il toner della porta è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c3cce-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="c3cce-135">\_stato di \_ riscaldamento della porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="c3cce-136">La stampante della porta si sta scaldando.</span><span class="sxs-lookup"><span data-stu-id="c3cce-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="c3cce-137">\_ \_ risparmio energia stato \_ porta</span><span class="sxs-lookup"><span data-stu-id="c3cce-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="c3cce-138">La stampante della porta è in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="c3cce-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c3cce-139">**pszStatus**</span><span class="sxs-lookup"><span data-stu-id="c3cce-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c3cce-140">Puntatore a una nuova stringa del valore dello stato della porta stampante da impostare.</span><span class="sxs-lookup"><span data-stu-id="c3cce-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="c3cce-141">Utilizzare questo membro se non esiste alcun valore di stato appropriato tra quelli elencati per **dwStatus**.</span><span class="sxs-lookup"><span data-stu-id="c3cce-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="c3cce-142">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="c3cce-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="c3cce-143">Gravità del valore dello stato della porta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-143">The severity of the port status value.</span></span>

<span data-ttu-id="c3cce-144">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3cce-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="c3cce-145">Valore</span><span class="sxs-lookup"><span data-stu-id="c3cce-145">Value</span></span>                       | <span data-ttu-id="c3cce-146">Significato</span><span class="sxs-lookup"><span data-stu-id="c3cce-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="c3cce-147">\_ \_ errore tipo di stato porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="c3cce-148">Il valore dello stato della porta indica un errore.</span><span class="sxs-lookup"><span data-stu-id="c3cce-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="c3cce-149">\_ \_ avviso tipo di stato porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="c3cce-150">Il valore dello stato della porta è un avviso.</span><span class="sxs-lookup"><span data-stu-id="c3cce-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="c3cce-151">\_informazioni sul \_ tipo di stato della porta \_</span><span class="sxs-lookup"><span data-stu-id="c3cce-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="c3cce-152">Il valore dello stato della porta è informativo.</span><span class="sxs-lookup"><span data-stu-id="c3cce-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3cce-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3cce-153">Remarks</span></span>

<span data-ttu-id="c3cce-154">Quando si imposta un valore di stato porta stampante con l' \_ errore tipo di stato porta valore gravità \_ \_ , lo spooler di stampa interrompe l'invio di processi alla porta.</span><span class="sxs-lookup"><span data-stu-id="c3cce-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="c3cce-155">Lo spooler di stampa non riprende l'invio di processi alla porta fino a quando non viene eseguita un'altra chiamata di [**porta**](setport.md) per cancellare lo stato.</span><span class="sxs-lookup"><span data-stu-id="c3cce-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cce-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3cce-156">Requirements</span></span>



| <span data-ttu-id="c3cce-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cce-157">Requirement</span></span> | <span data-ttu-id="c3cce-158">Valore</span><span class="sxs-lookup"><span data-stu-id="c3cce-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cce-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3cce-159">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cce-160">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3cce-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3cce-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3cce-161">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cce-162">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3cce-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3cce-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3cce-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3cce-164"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3cce-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c3cce-165">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c3cce-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c3cce-166">**\_ Informazioni sulla porta \_ \_ 3W** (Unicode) e **\_ informazioni sulla porta \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c3cce-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="c3cce-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3cce-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cce-168">Stampa</span><span class="sxs-lookup"><span data-stu-id="c3cce-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c3cce-169">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="c3cce-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c3cce-170">**Porta**</span><span class="sxs-lookup"><span data-stu-id="c3cce-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 





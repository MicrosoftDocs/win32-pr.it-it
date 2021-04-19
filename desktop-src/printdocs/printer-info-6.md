---
description: La stampante \_ info \_ 6 specifica il valore dello stato di una stampante.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Struttura PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318032"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="1e021-103">\_Struttura info stampa \_ 6</span><span class="sxs-lookup"><span data-stu-id="1e021-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="1e021-104">La **stampante \_ info \_ 6** specifica il valore dello stato di una stampante.</span><span class="sxs-lookup"><span data-stu-id="1e021-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e021-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e021-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="1e021-106">Members</span><span class="sxs-lookup"><span data-stu-id="1e021-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e021-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="1e021-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="1e021-108">Stato della stampante.</span><span class="sxs-lookup"><span data-stu-id="1e021-108">The printer status.</span></span> <span data-ttu-id="1e021-109">Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e021-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="1e021-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1e021-110">Value</span></span>                               | <span data-ttu-id="1e021-111">Significato</span><span class="sxs-lookup"><span data-stu-id="1e021-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e021-112">stato della stampante \_ \_ occupato</span><span class="sxs-lookup"><span data-stu-id="1e021-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="1e021-113">La stampante è occupata.</span><span class="sxs-lookup"><span data-stu-id="1e021-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="1e021-114">\_sportello dello stato della stampante \_ \_ aperto</span><span class="sxs-lookup"><span data-stu-id="1e021-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="1e021-115">Lo sportello della stampante è aperto.</span><span class="sxs-lookup"><span data-stu-id="1e021-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="1e021-116">\_errore di stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="1e021-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="1e021-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="1e021-118">\_inizializzazione dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="1e021-119">È in corso l'inizializzazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="1e021-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="1e021-120">\_io stato \_ stampante \_ attivo</span><span class="sxs-lookup"><span data-stu-id="1e021-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="1e021-121">La stampante è in uno stato di input/output attivo</span><span class="sxs-lookup"><span data-stu-id="1e021-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="1e021-122">\_feed manuale dello stato della stampante \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e021-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="1e021-123">La stampante è in uno stato di avanzamento manuale.</span><span class="sxs-lookup"><span data-stu-id="1e021-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="1e021-124">\_stato stampante \_ senza \_ toner</span><span class="sxs-lookup"><span data-stu-id="1e021-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="1e021-125">La stampante ha esaurito il toner.</span><span class="sxs-lookup"><span data-stu-id="1e021-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="1e021-126">stato della stampante \_ \_ non \_ disponibile</span><span class="sxs-lookup"><span data-stu-id="1e021-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="1e021-127">La stampante non è disponibile per la stampa.</span><span class="sxs-lookup"><span data-stu-id="1e021-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="1e021-128">stato della stampante \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="1e021-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="1e021-129">La stampante non è in linea.</span><span class="sxs-lookup"><span data-stu-id="1e021-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="1e021-130">\_ \_ \_ \_ memoria insufficiente per lo stato della stampante</span><span class="sxs-lookup"><span data-stu-id="1e021-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="1e021-131">Memoria esaurita per la stampante.</span><span class="sxs-lookup"><span data-stu-id="1e021-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="1e021-132">\_Cestino di \_ output stato stampante \_ \_ completo</span><span class="sxs-lookup"><span data-stu-id="1e021-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="1e021-133">Il cassetto di uscita della stampante è pieno.</span><span class="sxs-lookup"><span data-stu-id="1e021-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="1e021-134">pagina di stato della stampante \_ \_ \_ Punt</span><span class="sxs-lookup"><span data-stu-id="1e021-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="1e021-135">La stampante non è in grado di stampare la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="1e021-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="1e021-136">\_ \_ inceppamento carta stato stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="1e021-137">La carta è bloccata nella stampante</span><span class="sxs-lookup"><span data-stu-id="1e021-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="1e021-138">\_carta dello stato della stampante in \_ \_ uscita</span><span class="sxs-lookup"><span data-stu-id="1e021-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="1e021-139">La stampante ha esaurito la carta.</span><span class="sxs-lookup"><span data-stu-id="1e021-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="1e021-140">\_ \_ problema relativo alla carta di stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="1e021-141">La stampante presenta un problema relativo alla carta.</span><span class="sxs-lookup"><span data-stu-id="1e021-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="1e021-142">stato della stampante \_ \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="1e021-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="1e021-143">La stampante è sospesa.</span><span class="sxs-lookup"><span data-stu-id="1e021-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="1e021-144">\_stato stampante \_ in attesa di \_ eliminazione</span><span class="sxs-lookup"><span data-stu-id="1e021-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="1e021-145">La stampante è in attesa di eliminazione in seguito a una chiamata alla funzione [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="1e021-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="1e021-146">\_risparmio di stato della stampante \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e021-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="1e021-147">La stampante è in modalità risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="1e021-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="1e021-148">\_stampa dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="1e021-149">Viene stampata la stampante.</span><span class="sxs-lookup"><span data-stu-id="1e021-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="1e021-150">\_elaborazione dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="1e021-151">La stampante sta elaborando un comando dalla funzione [**Seprinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="1e021-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="1e021-152">\_Server stato \_ stampante \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="1e021-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="1e021-153">Lo stato della stampante è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1e021-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="1e021-154">\_ \_ toner stato stampante \_ basso</span><span class="sxs-lookup"><span data-stu-id="1e021-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="1e021-155">Il toner della stampante è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1e021-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="1e021-156">\_ \_ intervento dell'utente sullo stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="1e021-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="1e021-157">La stampante presenta un errore che richiede all'utente di eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="1e021-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="1e021-158">stato della stampante \_ \_ in attesa</span><span class="sxs-lookup"><span data-stu-id="1e021-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="1e021-159">La stampante è in attesa.</span><span class="sxs-lookup"><span data-stu-id="1e021-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="1e021-160">\_stato della \_ stampante \_ attivo</span><span class="sxs-lookup"><span data-stu-id="1e021-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="1e021-161">La stampante è in fase di riscaldamento.</span><span class="sxs-lookup"><span data-stu-id="1e021-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e021-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e021-162">Requirements</span></span>



| <span data-ttu-id="1e021-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e021-163">Requirement</span></span> | <span data-ttu-id="1e021-164">Valore</span><span class="sxs-lookup"><span data-stu-id="1e021-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e021-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e021-165">Minimum supported client</span></span><br/> | <span data-ttu-id="1e021-166">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e021-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e021-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e021-167">Minimum supported server</span></span><br/> | <span data-ttu-id="1e021-168">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e021-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e021-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e021-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e021-170"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e021-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1e021-171">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1e021-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1e021-172">**\_ \_ Info stampante \_ 6W** (Unicode) e **\_ \_ Info stampante \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1e021-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="1e021-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e021-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e021-174">Stampa</span><span class="sxs-lookup"><span data-stu-id="1e021-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1e021-175">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="1e021-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1e021-176">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="1e021-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="1e021-177">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1e021-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="1e021-178">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1e021-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="1e021-179">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1e021-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="1e021-180">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1e021-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="1e021-181">**\_Informazioni stampante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="1e021-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 





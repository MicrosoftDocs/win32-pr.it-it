---
description: La \_ struttura Printer Info \_ 4 specifica le informazioni generali sulla stampante. La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Struttura PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232894"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="69865-103">\_Struttura Info stampante \_ 4</span><span class="sxs-lookup"><span data-stu-id="69865-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="69865-104">La struttura **Printer \_ info \_ 4** specifica le informazioni generali sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="69865-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="69865-105">La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a [**EnumPrinters**](enumprinters.md).</span><span class="sxs-lookup"><span data-stu-id="69865-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="69865-106">Questa chiamata è un modo rapido e semplice per recuperare i nomi e gli attributi di tutte le stampanti installate localmente in un sistema e tutte le connessioni di stampanti remote stabilite da un utente.</span><span class="sxs-lookup"><span data-stu-id="69865-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="69865-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69865-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="69865-108">Members</span><span class="sxs-lookup"><span data-stu-id="69865-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69865-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="69865-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="69865-110">Puntatore a una stringa con terminazione null che specifica il nome della stampante (locale o remota).</span><span class="sxs-lookup"><span data-stu-id="69865-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="69865-111">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="69865-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="69865-112">Puntatore a una stringa con terminazione null che rappresenta il nome del server.</span><span class="sxs-lookup"><span data-stu-id="69865-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="69865-113">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="69865-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="69865-114">Specifica le informazioni sui dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="69865-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="69865-115">Valore</span><span class="sxs-lookup"><span data-stu-id="69865-115">Value</span></span>                       | <span data-ttu-id="69865-116">Significato</span><span class="sxs-lookup"><span data-stu-id="69865-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="69865-117">\_attributo stampante \_ locale</span><span class="sxs-lookup"><span data-stu-id="69865-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="69865-118">La stampante è una stampante locale.</span><span class="sxs-lookup"><span data-stu-id="69865-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="69865-119">\_rete attributi \_ stampante</span><span class="sxs-lookup"><span data-stu-id="69865-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="69865-120">La stampante è una stampante remota.</span><span class="sxs-lookup"><span data-stu-id="69865-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69865-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="69865-121">Remarks</span></span>

<span data-ttu-id="69865-122">La struttura delle **informazioni di stampa \_ \_ 4** fornisce un metodo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente.</span><span class="sxs-lookup"><span data-stu-id="69865-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="69865-123">Quando [**EnumPrinters**](enumprinters.md) viene chiamato con una struttura di dati **Printer \_ info \_ 4** , tale funzione esegue una query sul Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="69865-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="69865-124">Questo comportamento è diverso da quello di **EnumPrinters** quando viene chiamato con altri livelli di strutture di dati **\_ \_ xxx per informazioni sulla stampante** .</span><span class="sxs-lookup"><span data-stu-id="69865-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="69865-125">In particolare, quando **EnumPrinters** viene chiamato con una struttura di dati di livello 2 (**Printer \_ info \_ 2** ), esegue una chiamata **OpenPrinter** su ogni connessione remota.</span><span class="sxs-lookup"><span data-stu-id="69865-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="69865-126">Se una connessione remota è inattiva, se il server remoto non esiste più o se la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e, di conseguenza, interrompere la chiamata **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="69865-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="69865-127">L'operazione può richiedere un po' di tempo.</span><span class="sxs-lookup"><span data-stu-id="69865-127">This can take a while.</span></span> <span data-ttu-id="69865-128">Il passaggio di una struttura **Printer \_ info \_ 4** consente a un'applicazione di recuperare un minimo di informazioni obbligatorie; se si desidera ottenere informazioni più dettagliate, è possibile effettuare una chiamata di **EnumPrinter** Level 2 successiva.</span><span class="sxs-lookup"><span data-stu-id="69865-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="69865-129">**Gli attributi** possono inoltre contenere valori definiti nel campo **attributi** di **Printer \_ info \_ 2**.</span><span class="sxs-lookup"><span data-stu-id="69865-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="69865-130">Alcune configurazioni della stampante, ad esempio le connessioni alle stampanti ad alcuni server di stampa non basati su Windows, potrebbero restituire sia la **\_ \_ rete** locale degli attributi della stampante che l' **\_ \_ attributo Printer** .</span><span class="sxs-lookup"><span data-stu-id="69865-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="69865-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69865-131">Requirements</span></span>



| <span data-ttu-id="69865-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="69865-132">Requirement</span></span> | <span data-ttu-id="69865-133">Valore</span><span class="sxs-lookup"><span data-stu-id="69865-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69865-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69865-134">Minimum supported client</span></span><br/> | <span data-ttu-id="69865-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69865-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="69865-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69865-136">Minimum supported server</span></span><br/> | <span data-ttu-id="69865-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69865-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="69865-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69865-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="69865-139"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69865-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="69865-140">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="69865-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="69865-141">**\_ Informazioni sulla stampante \_ \_ 4W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="69865-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="69865-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69865-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69865-143">Stampa</span><span class="sxs-lookup"><span data-stu-id="69865-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="69865-144">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="69865-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="69865-145">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="69865-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="69865-146">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="69865-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="69865-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="69865-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="69865-148">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="69865-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="69865-149">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="69865-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="69865-150">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="69865-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 





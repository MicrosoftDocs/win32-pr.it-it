---
description: La \_ struttura Printer Info \_ 1 specifica le informazioni generali sulla stampante.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Struttura PRINTER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314001"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="ecfab-103">\_Struttura Info stampante \_ 1</span><span class="sxs-lookup"><span data-stu-id="ecfab-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="ecfab-104">La struttura **Printer \_ info \_ 1** specifica le informazioni generali sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="ecfab-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecfab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecfab-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ecfab-106">Members</span><span class="sxs-lookup"><span data-stu-id="ecfab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecfab-107">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ecfab-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ecfab-108">Specifica le informazioni sui dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="ecfab-108">Specifies information about the returned data.</span></span> <span data-ttu-id="ecfab-109">Di seguito sono riportati i valori di questo membro.</span><span class="sxs-lookup"><span data-stu-id="ecfab-109">Following are the values for this member.</span></span>



| <span data-ttu-id="ecfab-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ecfab-110">Value</span></span>                    | <span data-ttu-id="ecfab-111">Significato</span><span class="sxs-lookup"><span data-stu-id="ecfab-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfab-112">\_espansione enumerazione \_ stampanti</span><span class="sxs-lookup"><span data-stu-id="ecfab-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="ecfab-113">Un provider di stampa può impostare questo flag come hint per un'applicazione chiamante per enumerare ulteriormente questo oggetto se è abilitata l'espansione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ecfab-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="ecfab-114">Ad esempio, quando vengono enumerati i domini, un provider di stampa potrebbe indicare il dominio dell'utente impostando questo flag.</span><span class="sxs-lookup"><span data-stu-id="ecfab-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="ecfab-115">\_contenitore enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="ecfab-116">Se questo flag è impostato, l'oggetto stampante può contenere oggetti enumerabili.</span><span class="sxs-lookup"><span data-stu-id="ecfab-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="ecfab-117">Ad esempio, l'oggetto può essere un server di stampa che contiene stampanti.</span><span class="sxs-lookup"><span data-stu-id="ecfab-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="ecfab-118">\_ICON1 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="ecfab-119">Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come nome di rete di primo livello, ad esempio rete Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ecfab-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="ecfab-120">\_Icon2 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="ecfab-121">Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come dominio di rete.</span><span class="sxs-lookup"><span data-stu-id="ecfab-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="ecfab-122">\_ICON3 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="ecfab-123">Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come server di stampa.</span><span class="sxs-lookup"><span data-stu-id="ecfab-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="ecfab-124">\_ICON4 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="ecfab-125">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ecfab-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ecfab-126">\_ICON5 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="ecfab-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ecfab-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ecfab-128">\_ICON6 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="ecfab-129">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ecfab-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ecfab-130">\_Icon7 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="ecfab-131">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ecfab-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ecfab-132">\_ICON8 enum \_ Printer</span><span class="sxs-lookup"><span data-stu-id="ecfab-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="ecfab-133">Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come stampante.</span><span class="sxs-lookup"><span data-stu-id="ecfab-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="ecfab-134">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="ecfab-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="ecfab-135">Puntatore a una stringa con terminazione null che descrive il contenuto della struttura.</span><span class="sxs-lookup"><span data-stu-id="ecfab-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ecfab-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="ecfab-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ecfab-137">Puntatore a una stringa con terminazione null che assegna un nome al contenuto della struttura.</span><span class="sxs-lookup"><span data-stu-id="ecfab-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ecfab-138">**pComment**</span><span class="sxs-lookup"><span data-stu-id="ecfab-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="ecfab-139">Puntatore a una stringa con terminazione null che contiene dati aggiuntivi che descrivono la struttura.</span><span class="sxs-lookup"><span data-stu-id="ecfab-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecfab-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecfab-140">Requirements</span></span>



| <span data-ttu-id="ecfab-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecfab-141">Requirement</span></span> | <span data-ttu-id="ecfab-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ecfab-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfab-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecfab-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ecfab-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecfab-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ecfab-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecfab-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ecfab-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecfab-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ecfab-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecfab-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecfab-148"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecfab-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ecfab-149">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ecfab-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ecfab-150">**\_ \_ Info stampante \_ 1W** (Unicode) e **\_ \_ Info stampante \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ecfab-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ecfab-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecfab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecfab-152">Stampa</span><span class="sxs-lookup"><span data-stu-id="ecfab-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ecfab-153">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ecfab-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ecfab-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ecfab-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ecfab-155">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="ecfab-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="ecfab-156">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ecfab-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ecfab-157">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ecfab-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="ecfab-158">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ecfab-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 





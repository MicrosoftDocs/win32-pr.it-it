---
description: La \_ struttura delle impostazioni predefinite della stampante specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso per una stampante.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Struttura PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314010"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="bd561-103">\_Struttura delle impostazioni predefinite della stampante</span><span class="sxs-lookup"><span data-stu-id="bd561-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="bd561-104">La struttura delle **\_ impostazioni predefinite della stampante** specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso per una stampante.</span><span class="sxs-lookup"><span data-stu-id="bd561-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd561-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd561-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="bd561-106">Members</span><span class="sxs-lookup"><span data-stu-id="bd561-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd561-107">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="bd561-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="bd561-108">Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito per una stampante.</span><span class="sxs-lookup"><span data-stu-id="bd561-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="bd561-109">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="bd561-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="bd561-110">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che identifica l'ambiente predefinito e i dati di inizializzazione per una stampante.</span><span class="sxs-lookup"><span data-stu-id="bd561-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="bd561-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="bd561-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="bd561-112">Specifica i diritti di accesso desiderati per una stampante.</span><span class="sxs-lookup"><span data-stu-id="bd561-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="bd561-113">La funzione [**OpenPrinter**](openprinter.md) utilizza questo membro per impostare i diritti di accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="bd561-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="bd561-114">Questi diritti possono influire sul funzionamento delle funzioni [**Seprinter**](setprinter.md) e [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="bd561-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="bd561-115">I diritti di accesso possono essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="bd561-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="bd561-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bd561-116">Value</span></span>                                       | <span data-ttu-id="bd561-117">Significato</span><span class="sxs-lookup"><span data-stu-id="bd561-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd561-118">\_amministrazione dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="bd561-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="bd561-119">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="bd561-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="bd561-120">\_uso dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="bd561-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="bd561-121">Per eseguire operazioni di stampa di base.</span><span class="sxs-lookup"><span data-stu-id="bd561-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="bd561-122">\_gestione dell'accesso alla stampante \_ \_ limitata</span><span class="sxs-lookup"><span data-stu-id="bd561-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="bd561-123">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="bd561-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="bd561-124">Questo valore è disponibile a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="bd561-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="bd561-125">\_tutti gli \_ accessi alla stampante</span><span class="sxs-lookup"><span data-stu-id="bd561-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="bd561-126">Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione (vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="bd561-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="bd561-127">valori di sicurezza generici, ad esempio WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="bd561-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="bd561-128">Per consentire diritti di accesso di controllo specifici.</span><span class="sxs-lookup"><span data-stu-id="bd561-128">To allow specific control access rights.</span></span> <span data-ttu-id="bd561-129">Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="bd561-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd561-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd561-130">Requirements</span></span>



| <span data-ttu-id="bd561-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd561-131">Requirement</span></span> | <span data-ttu-id="bd561-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bd561-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd561-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd561-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bd561-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd561-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bd561-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd561-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bd561-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd561-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bd561-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd561-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd561-138"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd561-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bd561-139">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bd561-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bd561-140">**\_ Printer \_ DEFAULTSW** (Unicode) e **\_ Printer \_ DEFAULTSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bd561-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bd561-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd561-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd561-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="bd561-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bd561-143">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="bd561-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bd561-144">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="bd561-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="bd561-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="bd561-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="bd561-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bd561-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bd561-147">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bd561-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 


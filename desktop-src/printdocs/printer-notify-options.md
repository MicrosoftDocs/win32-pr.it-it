---
description: La \_ \_ struttura opzioni di notifica stampanti consente di specificare le opzioni per un oggetto notifica di modifica che monitora una stampante o un server di stampa.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Struttura PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313539"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="55d21-103">Struttura delle opzioni di \_ notifica stampanti \_</span><span class="sxs-lookup"><span data-stu-id="55d21-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="55d21-104">La **struttura \_ \_ Opzioni di notifica stampanti** consente di specificare le opzioni per un oggetto notifica di modifica che monitora una stampante o un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="55d21-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d21-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55d21-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="55d21-106">Members</span><span class="sxs-lookup"><span data-stu-id="55d21-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="55d21-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="55d21-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="55d21-108">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="55d21-108">The version of this structure.</span></span> <span data-ttu-id="55d21-109">Impostare questo membro su 2.</span><span class="sxs-lookup"><span data-stu-id="55d21-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="55d21-110">**Flag**</span><span class="sxs-lookup"><span data-stu-id="55d21-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="55d21-111">Flag di bit.</span><span class="sxs-lookup"><span data-stu-id="55d21-111">A bit flag.</span></span> <span data-ttu-id="55d21-112">Se si imposta il \_ flag di aggiornamento delle opzioni di notifica della stampante \_ \_ in una chiamata alla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la funzione fornisce i dati correnti per tutti i campi delle informazioni sulla stampante monitorata.</span><span class="sxs-lookup"><span data-stu-id="55d21-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="55d21-113">La funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora il membro dei **flag** .</span><span class="sxs-lookup"><span data-stu-id="55d21-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="55d21-114">**Count**</span><span class="sxs-lookup"><span data-stu-id="55d21-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="55d21-115">Numero di elementi nella matrice **pTypes** .</span><span class="sxs-lookup"><span data-stu-id="55d21-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="55d21-116">**pTypes**</span><span class="sxs-lookup"><span data-stu-id="55d21-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="55d21-117">Puntatore a una matrice di opzioni di notifica delle stampanti per le strutture dei [**\_ \_ \_ tipi**](printer-notify-options-type.md) .</span><span class="sxs-lookup"><span data-stu-id="55d21-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="55d21-118">Usare un elemento di questa matrice per specificare i campi delle informazioni sulla stampante da monitorare e un elemento per specificare i campi di informazioni sui processi da monitorare.</span><span class="sxs-lookup"><span data-stu-id="55d21-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="55d21-119">È possibile monitorare le informazioni sulle stampanti, le informazioni sui processi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="55d21-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55d21-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d21-120">Remarks</span></span>

<span data-ttu-id="55d21-121">Usare questa struttura con la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) per specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare per la modifica.</span><span class="sxs-lookup"><span data-stu-id="55d21-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="55d21-122">Usare questa struttura con la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) per richiedere i dati correnti per tutti i campi di informazioni sui processi e le stampanti monitorati.</span><span class="sxs-lookup"><span data-stu-id="55d21-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="55d21-123">In questo caso, il membro **Flags** specifica il \_ flag di aggiornamento delle opzioni di notifica della stampante \_ \_ e la funzione ignora gli altri membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="55d21-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d21-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d21-124">Requirements</span></span>



| <span data-ttu-id="55d21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d21-125">Requirement</span></span> | <span data-ttu-id="55d21-126">Valore</span><span class="sxs-lookup"><span data-stu-id="55d21-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d21-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d21-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55d21-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55d21-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="55d21-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d21-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55d21-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55d21-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="55d21-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55d21-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d21-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55d21-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d21-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55d21-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d21-134">Stampa</span><span class="sxs-lookup"><span data-stu-id="55d21-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="55d21-135">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="55d21-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="55d21-136">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="55d21-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="55d21-137">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="55d21-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="55d21-138">**\_tipo di \_ Opzioni di notifica stampanti \_**</span><span class="sxs-lookup"><span data-stu-id="55d21-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 





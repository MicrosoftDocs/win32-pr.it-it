---
description: La \_ struttura del \_ tipo di opzioni di notifica stampanti consente di \_ specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare tramite un oggetto notifica di modifica della stampante. Una chiamata alla funzione FindFirstPrinterChangeNotification specifica una \_ \_ struttura di opzioni di notifica della stampante, che contiene una matrice di \_ strutture di tipi di opzioni di notifica stampanti \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Struttura PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313542"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="ca7f2-103">\_Struttura del \_ tipo di opzioni di notifica stampanti \_</span><span class="sxs-lookup"><span data-stu-id="ca7f2-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="ca7f2-104">La struttura del **\_ tipo di \_ Opzioni \_ di notifica stampanti** consente di specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare tramite un oggetto notifica di modifica della stampante.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="ca7f2-105">Una chiamata alla funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) specifica una struttura [**di \_ \_ Opzioni di notifica della stampante**](printer-notify-options.md) , che contiene una matrice di strutture di **\_ \_ \_ tipi di opzioni di notifica stampanti** .</span><span class="sxs-lookup"><span data-stu-id="ca7f2-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7f2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca7f2-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="ca7f2-107">Members</span><span class="sxs-lookup"><span data-stu-id="ca7f2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca7f2-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-109">Tipo da guardare.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-109">The type to be watched.</span></span> <span data-ttu-id="ca7f2-110">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="ca7f2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ca7f2-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="ca7f2-112">Significato</span><span class="sxs-lookup"><span data-stu-id="ca7f2-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="ca7f2-113"><dt>**Processo \_ di Invia notifica al \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="ca7f2-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="ca7f2-114">Indica che i campi specificati nella matrice **pFields** sono costanti di \_ campo Notify di processo \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="ca7f2-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="ca7f2-115"><dt>**Stampante \_ NOTIFICA \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="ca7f2-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="ca7f2-116">Indica che i campi specificati nella matrice **pFields** sono costanti di \_ campo notifica stampanti \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="ca7f2-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ca7f2-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca7f2-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-120">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca7f2-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca7f2-123">**Count**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-124">Numero di elementi nella matrice **pFields** .</span><span class="sxs-lookup"><span data-stu-id="ca7f2-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="ca7f2-125">**pFields**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="ca7f2-126">Puntatore a una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-126">A pointer to an array of values.</span></span> <span data-ttu-id="ca7f2-127">Ogni elemento della matrice specifica un campo di informazioni su processo o stampante di interesse.</span><span class="sxs-lookup"><span data-stu-id="ca7f2-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="ca7f2-128">Per un elenco dei campi di informazioni sulle stampanti e sui processi supportati, vedere la pagina relativa alla struttura dei [**\_ \_ \_ dati di notifica della stampante**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="ca7f2-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca7f2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca7f2-129">Requirements</span></span>



| <span data-ttu-id="ca7f2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca7f2-130">Requirement</span></span> | <span data-ttu-id="ca7f2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ca7f2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7f2-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca7f2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ca7f2-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca7f2-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca7f2-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca7f2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ca7f2-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca7f2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca7f2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca7f2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca7f2-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca7f2-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca7f2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca7f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7f2-139">Stampa</span><span class="sxs-lookup"><span data-stu-id="ca7f2-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ca7f2-140">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ca7f2-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ca7f2-141">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="ca7f2-142">**\_dati delle \_ informazioni di notifica della stampante \_**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="ca7f2-143">**\_Opzioni di notifica stampanti \_**</span><span class="sxs-lookup"><span data-stu-id="ca7f2-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 





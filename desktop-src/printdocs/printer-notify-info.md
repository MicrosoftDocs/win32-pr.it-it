---
description: La \_ struttura delle \_ informazioni di notifica della stampante contiene informazioni sulle stampanti restituite dalla funzione FindNextPrinterChangeNotification. La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Struttura PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313543"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="4eb21-104">\_ \_ Struttura info notifica stampanti</span><span class="sxs-lookup"><span data-stu-id="4eb21-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="4eb21-105">La struttura delle **\_ \_ informazioni di notifica della stampante** contiene informazioni sulle stampanti restituite dalla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb21-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="4eb21-106">La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.</span><span class="sxs-lookup"><span data-stu-id="4eb21-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb21-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4eb21-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="4eb21-108">Members</span><span class="sxs-lookup"><span data-stu-id="4eb21-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4eb21-109">**Versione**</span><span class="sxs-lookup"><span data-stu-id="4eb21-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="4eb21-110">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="4eb21-110">The version of this structure.</span></span> <span data-ttu-id="4eb21-111">Impostare questo membro su 2.</span><span class="sxs-lookup"><span data-stu-id="4eb21-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="4eb21-112">**Flag**</span><span class="sxs-lookup"><span data-stu-id="4eb21-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4eb21-113">Flag di bit che indica lo stato della struttura di notifica.</span><span class="sxs-lookup"><span data-stu-id="4eb21-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="4eb21-114">Se il bit delle informazioni di notifica della stampante \_ \_ \_ non è impostato, viene indicato che alcune notifiche devono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="4eb21-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="4eb21-115">**Count**</span><span class="sxs-lookup"><span data-stu-id="4eb21-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="4eb21-116">Il numero di [**elementi \_ \_ \_ dati relativi alle informazioni di notifica della stampante**](printer-notify-info-data.md) nella matrice **ADATA** .</span><span class="sxs-lookup"><span data-stu-id="4eb21-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="4eb21-117">**aData**</span><span class="sxs-lookup"><span data-stu-id="4eb21-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="4eb21-118">Matrice di strutture [**di \_ \_ \_ dati**](printer-notify-info-data.md) per le informazioni di notifica delle stampanti.</span><span class="sxs-lookup"><span data-stu-id="4eb21-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="4eb21-119">Ogni elemento della matrice identifica un singolo campo di informazioni relative a processi o stampanti e fornisce i dati correnti per quel campo.</span><span class="sxs-lookup"><span data-stu-id="4eb21-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eb21-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eb21-120">Remarks</span></span>

<span data-ttu-id="4eb21-121">Se il membro **Flags** dispone del \_ set di bit della stampante Notify \_ info \_ scartato, indica che si è verificato un overflow o un errore e le notifiche potrebbero essere andate perse.</span><span class="sxs-lookup"><span data-stu-id="4eb21-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="4eb21-122">In questo caso, è necessario chiamare [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e specificare il \_ \_ flag di aggiornamento delle opzioni di notifica della stampante \_ per recuperare tutte le informazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="4eb21-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="4eb21-123">Fino a quando non verrà richiesta questa operazione di aggiornamento, il sistema non invierà altre notifiche per questo oggetto notifica di modifica.</span><span class="sxs-lookup"><span data-stu-id="4eb21-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb21-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eb21-124">Requirements</span></span>



| <span data-ttu-id="4eb21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb21-125">Requirement</span></span> | <span data-ttu-id="4eb21-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4eb21-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb21-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eb21-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb21-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4eb21-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4eb21-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eb21-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb21-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4eb21-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4eb21-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4eb21-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb21-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4eb21-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb21-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eb21-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb21-134">Stampa</span><span class="sxs-lookup"><span data-stu-id="4eb21-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4eb21-135">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4eb21-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4eb21-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="4eb21-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="4eb21-137">**\_dati delle \_ informazioni di notifica della stampante \_**</span><span class="sxs-lookup"><span data-stu-id="4eb21-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 





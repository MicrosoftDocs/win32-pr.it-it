---
description: La struttura della porta \_ info \_ 2 identifica una porta stampante supportata.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Struttura PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314532"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="995a7-103">Struttura delle informazioni sulla porta \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="995a7-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="995a7-104">La struttura della **porta \_ info \_ 2** identifica una porta stampante supportata.</span><span class="sxs-lookup"><span data-stu-id="995a7-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="995a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="995a7-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="995a7-106">Members</span><span class="sxs-lookup"><span data-stu-id="995a7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="995a7-107">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="995a7-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="995a7-108">Puntatore a una stringa con terminazione null che identifica una porta stampante supportata (ad esempio, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="995a7-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="995a7-109">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="995a7-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="995a7-110">Puntatore a una stringa con terminazione null che identifica un monitoraggio installato (ad esempio, "monitoraggio PJL").</span><span class="sxs-lookup"><span data-stu-id="995a7-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="995a7-111">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="995a7-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="995a7-112">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="995a7-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="995a7-113">Puntatore a una stringa con terminazione null che descrive la porta in modo più dettagliato (ad esempio, se **pPortName** è "LPT1:", **pDescription** è "Printer Port").</span><span class="sxs-lookup"><span data-stu-id="995a7-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="995a7-114">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="995a7-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="995a7-115">**fPortType**</span><span class="sxs-lookup"><span data-stu-id="995a7-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="995a7-116">Maschera di maschera che descrive il tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="995a7-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="995a7-117">Questo membro può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="995a7-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="995a7-118">**\_scrittura tipo \_ porta**</span><span class="sxs-lookup"><span data-stu-id="995a7-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="995a7-119">**\_tipo porta \_ letto**</span><span class="sxs-lookup"><span data-stu-id="995a7-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="995a7-120">**tipo di porta \_ \_ reindirizzato**</span><span class="sxs-lookup"><span data-stu-id="995a7-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="995a7-121">**tipo di porta \_ \_ net \_ Attached**</span><span class="sxs-lookup"><span data-stu-id="995a7-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="995a7-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="995a7-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="995a7-123">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="995a7-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="995a7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="995a7-124">Remarks</span></span>

<span data-ttu-id="995a7-125">Utilizzare la struttura **Port \_ info \_ 2** quando si chiama [**EnumPorts**](enumports.md) se sono installati più monitor che supportano le stesse porte.</span><span class="sxs-lookup"><span data-stu-id="995a7-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="995a7-126">È possibile eseguire una query sul membro **fPortType** per determinare le informazioni sulla porta.</span><span class="sxs-lookup"><span data-stu-id="995a7-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="995a7-127">Si noti che le impostazioni della porta non influenzano gli attributi della stampante (restituiti dal membro **Attributes** di [**Printer \_ info \_ 2**](printer-info-2.md)).</span><span class="sxs-lookup"><span data-stu-id="995a7-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="995a7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="995a7-128">Requirements</span></span>



| <span data-ttu-id="995a7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="995a7-129">Requirement</span></span> | <span data-ttu-id="995a7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="995a7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="995a7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="995a7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="995a7-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="995a7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="995a7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="995a7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="995a7-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="995a7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="995a7-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="995a7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="995a7-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="995a7-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="995a7-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="995a7-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="995a7-138">**\_ \_ Info porta \_ 2W** (Unicode) e **\_ porta \_ info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="995a7-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="995a7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="995a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995a7-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="995a7-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="995a7-141">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="995a7-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="995a7-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="995a7-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 





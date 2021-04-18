---
description: Contiene la data di produzione di una batteria.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Struttura BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312060"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="54324-103">Struttura della data di \_ produzione della batteria \_</span><span class="sxs-lookup"><span data-stu-id="54324-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="54324-104">Contiene la data di produzione di una batteria.</span><span class="sxs-lookup"><span data-stu-id="54324-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="54324-105">Questa struttura viene utilizzata dalla struttura [**di \_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) quando è richiesto il livello di informazioni BatteryManufactureDate.</span><span class="sxs-lookup"><span data-stu-id="54324-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="54324-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54324-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="54324-107">Members</span><span class="sxs-lookup"><span data-stu-id="54324-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="54324-108">**Day**</span><span class="sxs-lookup"><span data-stu-id="54324-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="54324-109">Giorno del mese di produzione, compreso tra 1 e 31.</span><span class="sxs-lookup"><span data-stu-id="54324-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="54324-110">Nonostante il tipo di dati, non si tratta di un valore con codifica ASCII.</span><span class="sxs-lookup"><span data-stu-id="54324-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="54324-111">Si tratta di un byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="54324-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="54324-112">**Mese**</span><span class="sxs-lookup"><span data-stu-id="54324-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="54324-113">Mese di produzione, compreso tra 1 (gennaio) e 12 (dicembre).</span><span class="sxs-lookup"><span data-stu-id="54324-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="54324-114">Nonostante il tipo di dati, non si tratta di un valore con codifica ASCII.</span><span class="sxs-lookup"><span data-stu-id="54324-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="54324-115">Si tratta di un byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="54324-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="54324-116">**Anno**</span><span class="sxs-lookup"><span data-stu-id="54324-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="54324-117">Anno di produzione.</span><span class="sxs-lookup"><span data-stu-id="54324-117">The year of manufacture.</span></span> <span data-ttu-id="54324-118">Questo sarà in genere compreso nell'intervallo 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="54324-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54324-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="54324-119">Remarks</span></span>

<span data-ttu-id="54324-120">La data è codificata nel formato calendario gregoriano o occidentale.</span><span class="sxs-lookup"><span data-stu-id="54324-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="54324-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54324-121">Requirements</span></span>



| <span data-ttu-id="54324-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="54324-122">Requirement</span></span> | <span data-ttu-id="54324-123">Valore</span><span class="sxs-lookup"><span data-stu-id="54324-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54324-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54324-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54324-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="54324-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="54324-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54324-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54324-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54324-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="54324-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54324-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="54324-129"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="54324-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54324-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54324-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54324-131">**\_informazioni sulle query della batteria \_**</span><span class="sxs-lookup"><span data-stu-id="54324-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="54324-132">**\_ \_ informazioni sulle query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="54324-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 





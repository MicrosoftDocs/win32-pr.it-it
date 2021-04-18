---
description: Fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i dati possibili inseriti in una colonna.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Struttura NMCOLUMNVARIANT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318967"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="6a7ef-103">Struttura NMCOLUMNVARIANT</span><span class="sxs-lookup"><span data-stu-id="6a7ef-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="6a7ef-104">La struttura **NMCOLUMNVARIANT** fornisce una riga nel riquadro superiore del Visualizzatore eventi che funge da contenitore per tutti i dati possibili inseriti in una colonna.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a7ef-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="6a7ef-106">Members</span><span class="sxs-lookup"><span data-stu-id="6a7ef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a7ef-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-108">Valore del tipo di enumerazione [**NMCOLUMNTYPE**](nmcolumntype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a7ef-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-109">**Valore**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a7ef-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-111">valore Unsigned Integer a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-113">valore intero con segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-115">valore Unsigned Integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-117">valore intero con segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-119">valore Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-121">valore intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-123">valore float a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-124">**FrameVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-125">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-126">**YesNoVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-127">Viene visualizzato Sì o no.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-128">**OnOffVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-129">Visualizza on o off.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-130">**TrueFalseVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-131">Visualizza true o false.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-132">**MACAddrVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-133">Indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-134">**IPXAddrVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-135">Indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-136">**IPAddrVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-137">Un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-138">**VarTimeVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-139">Tempo Variant.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-139">Variant time.</span></span> <span data-ttu-id="6a7ef-140">Usare **VariantTimetoSystemTime** per convertire l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ef-141">**pStringVal**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="6a7ef-142">Puntatore a una stringa.</span><span class="sxs-lookup"><span data-stu-id="6a7ef-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a7ef-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a7ef-143">Requirements</span></span>



| <span data-ttu-id="6a7ef-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a7ef-144">Requirement</span></span> | <span data-ttu-id="6a7ef-145">Valore</span><span class="sxs-lookup"><span data-stu-id="6a7ef-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7ef-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a7ef-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6a7ef-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a7ef-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6a7ef-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a7ef-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6a7ef-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a7ef-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a7ef-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a7ef-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a7ef-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ef-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7ef-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a7ef-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7ef-153">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="6a7ef-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 





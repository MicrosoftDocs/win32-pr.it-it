---
description: Specifica i membri della struttura NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Enumerazione NMCOLUMNTYPE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760124"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="7ab94-103">Enumerazione NMCOLUMNTYPE</span><span class="sxs-lookup"><span data-stu-id="7ab94-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="7ab94-104">L'enumerazione **NMCOLUMNTYPE** specifica i membri della struttura [**NMCOLUMNVARIANT**](nmcolumnvariant.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab94-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ab94-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="7ab94-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7ab94-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7ab94-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**\_Uint8 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-108">Unsigned Integer a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**\_SINT8 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-110">intero con segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ab94-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-112">Unsigned Integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**\_SINT16 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-114">intero con segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**\_UInt32 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-116">Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**\_SINT32 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-118">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**\_FLOAT64 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-120">float a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="7ab94-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**\_frame NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-122">Numero di frame.</span><span class="sxs-lookup"><span data-stu-id="7ab94-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**\_YesNo NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-124">"Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="7ab94-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**\_OnOff NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-126">"On" o "off"</span><span class="sxs-lookup"><span data-stu-id="7ab94-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**\_TRUEFALSE NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-128">"True" o "false".</span><span class="sxs-lookup"><span data-stu-id="7ab94-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**\_MACADDR NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-130">Indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="7ab94-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**\_IPXADDR NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-132">Indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="7ab94-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**\_IPADDR NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-134">Un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="7ab94-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**\_VARTIME NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-136">Tempo Variant.</span><span class="sxs-lookup"><span data-stu-id="7ab94-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="7ab94-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_stringa NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="7ab94-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="7ab94-138">Puntatore a una stringa.</span><span class="sxs-lookup"><span data-stu-id="7ab94-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ab94-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ab94-139">Requirements</span></span>



| <span data-ttu-id="7ab94-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab94-140">Requirement</span></span> | <span data-ttu-id="7ab94-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7ab94-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab94-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ab94-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab94-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ab94-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7ab94-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ab94-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab94-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ab94-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7ab94-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ab94-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab94-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab94-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 





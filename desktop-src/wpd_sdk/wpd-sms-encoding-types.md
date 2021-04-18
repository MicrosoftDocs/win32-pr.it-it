---
description: Il \_ \_ \_ tipo di enumerazione WPD SMS Encoding types descrive il tipo di codifica di un messaggio SMS (Short Message Service).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumerazione WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331721"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="50c9d-103">\_ \_ Enumerazione tipi di codifica SMS di WPD \_</span><span class="sxs-lookup"><span data-stu-id="50c9d-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="50c9d-104">Il tipo di enumerazione **WPD \_ SMS \_ Encoding \_ types** descrive il tipo di codifica di un messaggio SMS (Short Message Service).</span><span class="sxs-lookup"><span data-stu-id="50c9d-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c9d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50c9d-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="50c9d-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="50c9d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50c9d-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Codifica SMS \_ 7 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="50c9d-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="50c9d-108">Codifica a sette bit.</span><span class="sxs-lookup"><span data-stu-id="50c9d-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="50c9d-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**\_Codifica SMS \_ 8 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="50c9d-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="50c9d-110">Codifica a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="50c9d-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="50c9d-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Codifica SMS \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="50c9d-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="50c9d-112">Codifica a 16 bit (UTF).</span><span class="sxs-lookup"><span data-stu-id="50c9d-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50c9d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="50c9d-113">Remarks</span></span>

<span data-ttu-id="50c9d-114">Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ codifica SMS di WPD](sms-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="50c9d-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c9d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50c9d-115">Requirements</span></span>



| <span data-ttu-id="50c9d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50c9d-116">Requirement</span></span> | <span data-ttu-id="50c9d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="50c9d-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c9d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50c9d-118">Header</span></span><br/> | <dl> <span data-ttu-id="50c9d-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="50c9d-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c9d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50c9d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c9d-121">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="50c9d-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





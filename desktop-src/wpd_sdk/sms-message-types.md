---
description: Il \_ \_ tipo di enumerazione dei tipi di messaggio SMS descrive il tipo di contenuto di un messaggio SMS (Short Message Service).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Enumerazione SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326596"
---
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="945fb-103">\_Enumerazione tipi di messaggio SMS \_</span><span class="sxs-lookup"><span data-stu-id="945fb-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="945fb-104">Il tipo di enumerazione dei **\_ \_ tipi di messaggio SMS** descrive il tipo di contenuto di un messaggio SMS (Short Message Service).</span><span class="sxs-lookup"><span data-stu-id="945fb-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="945fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="945fb-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="945fb-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="945fb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="945fb-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="945fb-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="945fb-108">Messaggio di testo.</span><span class="sxs-lookup"><span data-stu-id="945fb-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="945fb-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_messaggio binario \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="945fb-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="945fb-110">Messaggio binario.</span><span class="sxs-lookup"><span data-stu-id="945fb-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="945fb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="945fb-111">Remarks</span></span>

<span data-ttu-id="945fb-112">Questa enumerazione viene utilizzata dal comando [**WPD \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).</span><span class="sxs-lookup"><span data-stu-id="945fb-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="945fb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="945fb-113">Requirements</span></span>



| <span data-ttu-id="945fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="945fb-114">Requirement</span></span> | <span data-ttu-id="945fb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="945fb-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="945fb-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="945fb-116">Header</span></span><br/> | <dl> <span data-ttu-id="945fb-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="945fb-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945fb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="945fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945fb-119">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="945fb-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





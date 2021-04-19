---
description: I dispositivi portatili Windows supportano le proprietà SMS seguenti.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Proprietà SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326595"
---
# <a name="sms-properties"></a><span data-ttu-id="d0918-103">Proprietà SMS</span><span class="sxs-lookup"><span data-stu-id="d0918-103">SMS Properties</span></span>

<span data-ttu-id="d0918-104">I dispositivi portatili Windows supportano le proprietà SMS seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0918-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="d0918-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d0918-105">Property</span></span>                   | <span data-ttu-id="d0918-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d0918-106">VarType</span></span>        | <span data-ttu-id="d0918-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0918-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0918-108">**\_codifica SMS \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d0918-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="d0918-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="d0918-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d0918-110">Valore che specifica il modo in cui il driver codificherà il messaggio di testo inviato dal client.</span><span class="sxs-lookup"><span data-stu-id="d0918-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="d0918-111">Si tratta di una proprietà di sola lettura. il client non è in grado di specificare il tipo di codifica utilizzato da un dispositivo per l'invio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="d0918-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="d0918-112">Questi valori duplicano i valori enumerati dei [**\_ \_ \_ tipi di codifica SMS di WPD**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="d0918-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="d0918-113">**\_ \_ payload max SMS \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d0918-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="d0918-114">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d0918-114">**VT\_UI4**</span></span>    | <span data-ttu-id="d0918-115">Numero massimo di byte che possono essere contenuti in un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d0918-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="d0918-116">**\_provider SMS \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d0918-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="d0918-117">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="d0918-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d0918-118">Nome del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="d0918-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d0918-119">**\_timeout SMS \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d0918-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="d0918-120">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="d0918-120">**VT\_UI4**</span></span>    | <span data-ttu-id="d0918-121">Numero di millisecondi fino alla restituzione di un timeout.</span><span class="sxs-lookup"><span data-stu-id="d0918-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="d0918-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0918-122">Requirements</span></span>



| <span data-ttu-id="d0918-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0918-123">Requirement</span></span> | <span data-ttu-id="d0918-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d0918-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0918-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0918-125">Header</span></span><br/> | <dl> <span data-ttu-id="d0918-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0918-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0918-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0918-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0918-128">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="d0918-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





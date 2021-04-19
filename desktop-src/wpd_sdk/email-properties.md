---
description: Dispositivi portatili Windows supporta le seguenti proprietà di posta elettronica.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Proprietà posta elettronica (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328969"
---
# <a name="email-properties"></a><span data-ttu-id="b18a1-103">Proprietà posta elettronica</span><span class="sxs-lookup"><span data-stu-id="b18a1-103">Email Properties</span></span>

<span data-ttu-id="b18a1-104">Dispositivi portatili Windows supporta le seguenti proprietà di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b18a1-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="b18a1-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b18a1-105">Property</span></span>                         | <span data-ttu-id="b18a1-106">VarType</span><span class="sxs-lookup"><span data-stu-id="b18a1-106">VarType</span></span>        | <span data-ttu-id="b18a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b18a1-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b18a1-108">**WPD \_ - \_ linea Ccn posta elettronica \_**</span><span class="sxs-lookup"><span data-stu-id="b18a1-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="b18a1-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b18a1-110">Destinatari Ccn del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b18a1-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="b18a1-111">I destinatari Ccn ricevono una copia del messaggio di posta elettronica, ma i relativi nomi non vengono visualizzati come destinatari.</span><span class="sxs-lookup"><span data-stu-id="b18a1-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="b18a1-112">**\_linea CC di posta elettronica WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b18a1-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="b18a1-113">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b18a1-114">Destinatari CC del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b18a1-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="b18a1-115">I destinatari CC ricevono una copia del messaggio di posta elettronica e i relativi nomi vengono visualizzati come destinatari.</span><span class="sxs-lookup"><span data-stu-id="b18a1-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="b18a1-116">**WPD \_ posta elettronica \_ con \_ allegati**</span><span class="sxs-lookup"><span data-stu-id="b18a1-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="b18a1-117">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="b18a1-118">Valore booleano che specifica se questo messaggio di posta elettronica contiene allegati.</span><span class="sxs-lookup"><span data-stu-id="b18a1-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="b18a1-119">**il \_ messaggio di posta elettronica WPD \_ è \_ stato \_ letto**</span><span class="sxs-lookup"><span data-stu-id="b18a1-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="b18a1-120">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="b18a1-121">Valore booleano che specifica se il messaggio di posta elettronica è stato letto.</span><span class="sxs-lookup"><span data-stu-id="b18a1-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="b18a1-122">**WPD \_ \_ tempo di ricezione posta elettronica \_**</span><span class="sxs-lookup"><span data-stu-id="b18a1-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="b18a1-123">**\_Data VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-123">**VT\_DATE**</span></span>   | <span data-ttu-id="b18a1-124">Valore che specifica quando è stato ricevuto il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b18a1-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="b18a1-125">**\_indirizzo mittente di posta elettronica WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b18a1-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="b18a1-126">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b18a1-127">Indirizzo di posta elettronica del mittente.</span><span class="sxs-lookup"><span data-stu-id="b18a1-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="b18a1-128">**WPD \_ posta elettronica \_ alla \_ riga**</span><span class="sxs-lookup"><span data-stu-id="b18a1-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="b18a1-129">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="b18a1-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b18a1-130">Destinatari principali del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b18a1-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="b18a1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b18a1-131">Requirements</span></span>



| <span data-ttu-id="b18a1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18a1-132">Requirement</span></span> | <span data-ttu-id="b18a1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b18a1-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b18a1-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b18a1-134">Header</span></span><br/> | <dl> <span data-ttu-id="b18a1-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b18a1-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18a1-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b18a1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18a1-137">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="b18a1-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





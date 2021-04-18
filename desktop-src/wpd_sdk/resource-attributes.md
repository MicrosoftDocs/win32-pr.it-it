---
description: I dispositivi portatili Windows supportano i seguenti attributi di risorse.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Attributi della risorsa (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332106"
---
# <a name="resource-attributes"></a><span data-ttu-id="46fdc-103">Attributi delle risorse</span><span class="sxs-lookup"><span data-stu-id="46fdc-103">Resource Attributes</span></span>

<span data-ttu-id="46fdc-104">I dispositivi portatili Windows supportano i seguenti attributi di risorse.</span><span class="sxs-lookup"><span data-stu-id="46fdc-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="46fdc-105">Questi attributi vengono restituiti dai metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="46fdc-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="46fdc-106">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="46fdc-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="46fdc-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="46fdc-107">Attribute</span></span>                                                  | <span data-ttu-id="46fdc-108">VarType</span><span class="sxs-lookup"><span data-stu-id="46fdc-108">VarType</span></span>      | <span data-ttu-id="46fdc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46fdc-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46fdc-110">**l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="46fdc-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="46fdc-111">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-111">**VT\_BOOL**</span></span> | <span data-ttu-id="46fdc-112">Valore booleano che specifica se un client dispone dell'autorizzazione per eliminare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="46fdc-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="46fdc-113">Se assente, si presuppone che sia false.</span><span class="sxs-lookup"><span data-stu-id="46fdc-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="46fdc-114">**l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere**</span><span class="sxs-lookup"><span data-stu-id="46fdc-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="46fdc-115">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-115">**VT\_BOOL**</span></span> | <span data-ttu-id="46fdc-116">Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="46fdc-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="46fdc-117">Se assente, si presuppone che sia false.</span><span class="sxs-lookup"><span data-stu-id="46fdc-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="46fdc-118">**l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere**</span><span class="sxs-lookup"><span data-stu-id="46fdc-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="46fdc-119">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-119">**VT\_BOOL**</span></span> | <span data-ttu-id="46fdc-120">Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="46fdc-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="46fdc-121">Se assente, si presuppone che sia false.</span><span class="sxs-lookup"><span data-stu-id="46fdc-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="46fdc-122">**\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD**</span><span class="sxs-lookup"><span data-stu-id="46fdc-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="46fdc-123">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-123">**VT\_UI4**</span></span>  | <span data-ttu-id="46fdc-124">Dimensione del buffer consigliata che un chiamante deve usare per le letture memorizzate nel buffer dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="46fdc-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="46fdc-125">**\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="46fdc-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="46fdc-126">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-126">**VT\_UI4**</span></span>  | <span data-ttu-id="46fdc-127">Dimensione del buffer consigliata che un chiamante deve usare per le scritture memorizzate nel buffer sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="46fdc-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="46fdc-128">**\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46fdc-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="46fdc-129">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="46fdc-129">**VT\_UI8**</span></span>  | <span data-ttu-id="46fdc-130">Dimensioni totali, in byte, dei dati della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46fdc-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="46fdc-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46fdc-131">Requirements</span></span>



| <span data-ttu-id="46fdc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="46fdc-132">Requirement</span></span> | <span data-ttu-id="46fdc-133">Valore</span><span class="sxs-lookup"><span data-stu-id="46fdc-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="46fdc-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46fdc-134">Header</span></span><br/> | <dl> <span data-ttu-id="46fdc-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="46fdc-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46fdc-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46fdc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fdc-137">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="46fdc-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





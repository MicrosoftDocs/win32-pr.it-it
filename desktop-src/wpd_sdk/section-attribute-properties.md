---
description: I dispositivi portatili Windows supportano le proprietà dei dati della sezione seguente.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Proprietà dell'attributo Section (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332372"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="f256c-103">Proprietà dell'attributo Section</span><span class="sxs-lookup"><span data-stu-id="f256c-103">Section Attribute Properties</span></span>

<span data-ttu-id="f256c-104">I dispositivi portatili Windows supportano le proprietà dei dati della sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="f256c-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="f256c-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f256c-105">Property</span></span>                                             | <span data-ttu-id="f256c-106">VarType</span><span class="sxs-lookup"><span data-stu-id="f256c-106">VarType</span></span>         | <span data-ttu-id="f256c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f256c-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f256c-108">**\_ \_ lunghezza dei dati della sezione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f256c-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="f256c-109">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="f256c-109">**VT\_UI8**</span></span>     | <span data-ttu-id="f256c-110">Specifica la lunghezza dell'oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="f256c-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f256c-111">**\_ \_ offset dati della sezione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f256c-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="f256c-112">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="f256c-112">**VT\_UI8**</span></span>     | <span data-ttu-id="f256c-113">Specifica l'offset in base zero dei dati per l'oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="f256c-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f256c-114">**\_ \_ \_ risorsa oggetto a cui si fa riferimento dati \_ della sezione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f256c-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="f256c-115">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f256c-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="f256c-116">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore che specifica la chiave per una determinata risorsa. Questa risorsa è l'oggetto a cui fa riferimento \_ l' \_ offset dei dati della sezione WPD \_ e la \_ \_ lunghezza dei dati della sezione WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="f256c-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="f256c-117">Se questa proprietà non esiste, \_ \_ viene utilizzata l'impostazione predefinita della risorsa WPD.</span><span class="sxs-lookup"><span data-stu-id="f256c-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="f256c-118">**\_ \_ unità dati della sezione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f256c-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="f256c-119">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="f256c-119">**VT\_UI4**</span></span>     | <span data-ttu-id="f256c-120">Specifica le unità usate per questo offset, ad esempio, byte, millisecondi e così via. I valori possibili per questa proprietà sono definiti nell'enumerazione **WPD \_ Section \_ data \_ unit \_ values** nel file portabledevice. h.</span><span class="sxs-lookup"><span data-stu-id="f256c-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="f256c-121">Se non viene specificata alcuna unità, vengono considerati i byte.</span><span class="sxs-lookup"><span data-stu-id="f256c-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="f256c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f256c-122">Requirements</span></span>



| <span data-ttu-id="f256c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f256c-123">Requirement</span></span> | <span data-ttu-id="f256c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f256c-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f256c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f256c-125">Header</span></span><br/> | <dl> <span data-ttu-id="f256c-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f256c-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f256c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f256c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f256c-128">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="f256c-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





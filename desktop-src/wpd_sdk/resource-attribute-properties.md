---
description: Dispositivi portatili Windows supporta le seguenti proprietà dell'attributo di risorsa.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Proprietà degli attributi delle risorse (PortableDevice. h)
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
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332107"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="46a35-103">Proprietà degli attributi delle risorse</span><span class="sxs-lookup"><span data-stu-id="46a35-103">Resource Attribute Properties</span></span>

<span data-ttu-id="46a35-104">Dispositivi portatili Windows supporta le seguenti proprietà dell'attributo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="46a35-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="46a35-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46a35-105">Property</span></span>                                    | <span data-ttu-id="46a35-106">VarType</span><span class="sxs-lookup"><span data-stu-id="46a35-106">VarType</span></span>         | <span data-ttu-id="46a35-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46a35-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a35-108">**\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46a35-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="46a35-109">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="46a35-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="46a35-110">Si tratta di un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore, ovvero la chiave che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="46a35-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="46a35-111">**\_formato dell' \_ attributo della risorsa WPD \_**</span><span class="sxs-lookup"><span data-stu-id="46a35-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="46a35-112">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="46a35-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="46a35-113">Valore GUID che specifica il formato della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46a35-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="46a35-114">Vedere [formati oggetto](object-format-guids.md) per un elenco di formati definiti da dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="46a35-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="46a35-115">**\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46a35-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="46a35-116">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="46a35-116">**VT\_UI8**</span></span>     | <span data-ttu-id="46a35-117">Dimensioni totali, in byte, dei dati della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46a35-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="46a35-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="46a35-118">Remarks</span></span>

<span data-ttu-id="46a35-119">Questi attributi vengono restituiti dal metodo [**IPortableDeviceResources:: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="46a35-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46a35-120">Requirements</span></span>



| <span data-ttu-id="46a35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a35-121">Requirement</span></span> | <span data-ttu-id="46a35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="46a35-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a35-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46a35-123">Header</span></span><br/> | <dl> <span data-ttu-id="46a35-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="46a35-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46a35-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46a35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a35-126">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="46a35-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="46a35-127">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="46a35-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





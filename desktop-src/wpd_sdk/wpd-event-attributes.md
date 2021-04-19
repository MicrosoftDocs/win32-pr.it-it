---
description: 'Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per gli eventi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Attributi evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324204"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="3b697-104">Attributi evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="3b697-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="3b697-105">Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per gli eventi di un servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b697-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="3b697-106">Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .</span><span class="sxs-lookup"><span data-stu-id="3b697-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="3b697-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="3b697-107">Attribute</span></span>                             | <span data-ttu-id="3b697-108">VarType</span><span class="sxs-lookup"><span data-stu-id="3b697-108">VarType</span></span>         | <span data-ttu-id="3b697-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b697-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b697-110">**\_nome dell' \_ attributo dell'evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b697-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="3b697-111">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="3b697-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="3b697-112">Stringa che specifica il nome descrittivo per lo script dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3b697-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="3b697-113">I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.</span><span class="sxs-lookup"><span data-stu-id="3b697-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="3b697-114">**\_Opzioni degli \_ attributi \_ evento WPD**</span><span class="sxs-lookup"><span data-stu-id="3b697-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="3b697-115">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="3b697-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3b697-116">Oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene le opzioni dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3b697-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="3b697-117">**\_parametri dell' \_ attributo dell'evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b697-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="3b697-118">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="3b697-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3b697-119">Oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3b697-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="3b697-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b697-120">Requirements</span></span>



| <span data-ttu-id="3b697-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b697-121">Requirement</span></span> | <span data-ttu-id="3b697-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3b697-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b697-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b697-123">Header</span></span><br/> | <dl> <span data-ttu-id="3b697-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b697-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b697-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b697-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b697-126">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="3b697-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





---
description: 'Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per i metodi di un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Attributi di metodo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326955"
---
# <a name="method-attributes"></a><span data-ttu-id="0dee4-104">Attributi del metodo</span><span class="sxs-lookup"><span data-stu-id="0dee4-104">Method Attributes</span></span>

<span data-ttu-id="0dee4-105">Per Windows 7, i dispositivi portatili Windows supportano gli attributi seguenti per i metodi di un servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dee4-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="0dee4-106">Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .</span><span class="sxs-lookup"><span data-stu-id="0dee4-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="0dee4-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="0dee4-107">Attribute</span></span>                                      | <span data-ttu-id="0dee4-108">VarType</span><span class="sxs-lookup"><span data-stu-id="0dee4-108">VarType</span></span>         | <span data-ttu-id="0dee4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dee4-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dee4-110">**\_ \_ accesso all'attributo del metodo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0dee4-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="0dee4-111">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="0dee4-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="0dee4-112">Accesso al metodo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0dee4-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="0dee4-113">**\_ \_ \_ formato associato all'attributo del metodo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0dee4-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="0dee4-114">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="0dee4-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="0dee4-115">Formato associato al metodo o **GUID \_ null** se non è associato alcun formato.</span><span class="sxs-lookup"><span data-stu-id="0dee4-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="0dee4-116">**\_ \_ nome attributo metodo \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="0dee4-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="0dee4-117">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="0dee4-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="0dee4-118">Stringa che specifica il nome descrittivo per lo script del metodo.</span><span class="sxs-lookup"><span data-stu-id="0dee4-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="0dee4-119">I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.</span><span class="sxs-lookup"><span data-stu-id="0dee4-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="0dee4-120">**\_parametri dell' \_ attributo del metodo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0dee4-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="0dee4-121">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="0dee4-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="0dee4-122">Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che contiene i parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="0dee4-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="0dee4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dee4-123">Requirements</span></span>



| <span data-ttu-id="0dee4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dee4-124">Requirement</span></span> | <span data-ttu-id="0dee4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0dee4-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dee4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dee4-126">Header</span></span><br/> | <dl> <span data-ttu-id="0dee4-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dee4-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dee4-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dee4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dee4-129">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="0dee4-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





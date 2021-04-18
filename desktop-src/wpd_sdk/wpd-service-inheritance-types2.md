---
description: Specifica la relazione di ereditarietà per un servizio.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: Enumerazione WPD_SERVICE_INHERITANCE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325103"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="4f4e5-103">\_ \_ Enumerazione tipi ereditarietà servizio WPD \_</span><span class="sxs-lookup"><span data-stu-id="4f4e5-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="4f4e5-104">Il tipo di enumerazione dei **\_ tipi di \_ ereditarietà \_ del servizio WPD** specifica la relazione di ereditarietà per un servizio.</span><span class="sxs-lookup"><span data-stu-id="4f4e5-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f4e5-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="4f4e5-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="4f4e5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4f4e5-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implementazione dell' \_ ereditarietà del servizio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="4f4e5-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e5-108">Il servizio eredita implementando una definizione del servizio abstract.</span><span class="sxs-lookup"><span data-stu-id="4f4e5-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f4e5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f4e5-109">Requirements</span></span>



| <span data-ttu-id="4f4e5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4e5-110">Requirement</span></span> | <span data-ttu-id="4f4e5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4f4e5-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4e5-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f4e5-112">Header</span></span><br/> | <dl> <span data-ttu-id="4f4e5-113"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4e5-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4e5-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f4e5-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4e5-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span><span class="sxs-lookup"><span data-stu-id="4f4e5-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 





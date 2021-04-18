---
description: Il \_ tipo di \_ enumerazione opzioni oggetto Delete descrive le opzioni supportate da un dispositivo durante l'eliminazione di un oggetto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Enumerazione DELETE_OBJECT_OPTIONS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328981"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="46fb7-103">\_Enumerazione Delete Object \_ Options</span><span class="sxs-lookup"><span data-stu-id="46fb7-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="46fb7-104">Il tipo di enumerazione **\_ \_ Opzioni oggetto Delete** descrive le opzioni supportate da un dispositivo durante l'eliminazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="46fb7-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fb7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46fb7-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="46fb7-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="46fb7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46fb7-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_non è \_ possibile eliminare la \_ \_ ricorsione del dispositivo portatile**</span><span class="sxs-lookup"><span data-stu-id="46fb7-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="46fb7-108">Eliminare l'oggetto solo e avere esito negativo se sono presenti elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="46fb7-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="46fb7-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ eliminazione di dispositivi portatili \_ con \_ ricorsione**</span><span class="sxs-lookup"><span data-stu-id="46fb7-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="46fb7-110">Eliminare l'oggetto e tutti i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="46fb7-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46fb7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="46fb7-111">Remarks</span></span>

<span data-ttu-id="46fb7-112">L'applicazione può recuperare le opzioni di eliminazione supportate dal dispositivo chiamando [**IPortableDeviceCapabilities:: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) per il comando **WPD \_ Command \_ Object \_ Management \_ Delete \_ objects** .</span><span class="sxs-lookup"><span data-stu-id="46fb7-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="46fb7-113">Deve esaminare il valore dell'opzione di **\_ \_ \_ \_ eliminazione ricorsiva \_ \_ supportata dall'opzione WPD** che questo metodo restituisce in un oggetto [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .</span><span class="sxs-lookup"><span data-stu-id="46fb7-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="46fb7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46fb7-114">Requirements</span></span>



| <span data-ttu-id="46fb7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="46fb7-115">Requirement</span></span> | <span data-ttu-id="46fb7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="46fb7-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="46fb7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46fb7-117">Header</span></span><br/> | <dl> <span data-ttu-id="46fb7-118"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="46fb7-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46fb7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46fb7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fb7-120">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="46fb7-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 





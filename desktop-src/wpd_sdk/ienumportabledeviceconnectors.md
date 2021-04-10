---
description: Supporta l'enumerazione delle interfacce IPortableDeviceConnector, che rappresentano i dispositivi MTP/Bluetooth associati al PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interfaccia IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231575"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="24a4e-103">Interfaccia IEnumPortableDeviceConnectors</span><span class="sxs-lookup"><span data-stu-id="24a4e-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="24a4e-104">L'interfaccia **IEnumPortableDeviceConnectors** supporta l'enumerazione delle interfacce [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , che rappresentano i dispositivi MTP/Bluetooth associati al PC.</span><span class="sxs-lookup"><span data-stu-id="24a4e-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="24a4e-105">Si noti che questa operazione recupererà tutti i dispositivi precedentemente associati, inclusi i dispositivi abbinati ma disconnessi.</span><span class="sxs-lookup"><span data-stu-id="24a4e-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="24a4e-106">Per determinare se un dispositivo è ancora connesso, eseguire una query sulla proprietà **DEVPKEY \_ MTPBTH \_ disconnected** per tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24a4e-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="24a4e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="24a4e-107">Members</span></span>

<span data-ttu-id="24a4e-108">L'interfaccia **IEnumPortableDeviceConnectors** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="24a4e-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24a4e-109">**IEnumPortableDeviceConnectors** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="24a4e-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="24a4e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="24a4e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24a4e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="24a4e-111">Methods</span></span>

<span data-ttu-id="24a4e-112">L'interfaccia **IEnumPortableDeviceConnectors** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="24a4e-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="24a4e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="24a4e-113">Method</span></span>                                               | <span data-ttu-id="24a4e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24a4e-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24a4e-115">**Clone**</span><span class="sxs-lookup"><span data-stu-id="24a4e-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="24a4e-116">Crea una copia dell'interfaccia **IEnumPortableDeviceConnectors** corrente.</span><span class="sxs-lookup"><span data-stu-id="24a4e-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="24a4e-117">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="24a4e-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="24a4e-118">Recupera uno o più oggetti [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) successivi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="24a4e-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="24a4e-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="24a4e-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="24a4e-120">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="24a4e-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="24a4e-121">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="24a4e-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="24a4e-122">Ignora il numero specificato di dispositivi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="24a4e-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="24a4e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24a4e-123">Requirements</span></span>



| <span data-ttu-id="24a4e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a4e-124">Requirement</span></span> | <span data-ttu-id="24a4e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="24a4e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a4e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24a4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="24a4e-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="24a4e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="24a4e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24a4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="24a4e-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24a4e-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="24a4e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24a4e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a4e-131"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a4e-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="24a4e-132">IDL</span><span class="sxs-lookup"><span data-stu-id="24a4e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24a4e-133"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24a4e-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="24a4e-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="24a4e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="24a4e-135"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a4e-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 


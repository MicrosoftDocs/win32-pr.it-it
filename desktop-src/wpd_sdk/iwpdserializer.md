---
description: "L'interfaccia IWpdSerializer viene utilizzata dal driver di dispositivo per serializzare le interfacce IPortableDeviceValues da e verso i buffer dei dati non elaborati utilizzati per comunicare con l'applicazione. Non è necessario che le applicazioni utilizzino questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente durante la chiamata a IPortableDevice:: SendCommand. per ottenere questa interfaccia, chiamare CoCreateInstance e passare IID \\_ IWpdSerializer."
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaccia IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330431"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="4361f-103">Interfaccia IWpdSerializer</span><span class="sxs-lookup"><span data-stu-id="4361f-103">IWpdSerializer interface</span></span>

<span data-ttu-id="4361f-104">L'interfaccia **IWpdSerializer** viene utilizzata dal driver di dispositivo per serializzare le interfacce [**IPortableDeviceValues**](iportabledevicevalues.md) da e verso i buffer dei dati non elaborati utilizzati per comunicare con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4361f-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="4361f-105">Non è necessario che le applicazioni utilizzino questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente quando si chiama [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="4361f-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="4361f-106">Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare l' **IID \_ IWpdSerializer**.</span><span class="sxs-lookup"><span data-stu-id="4361f-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="4361f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="4361f-107">Members</span></span>

<span data-ttu-id="4361f-108">L'interfaccia **IWpdSerializer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4361f-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4361f-109">**IWpdSerializer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4361f-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="4361f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="4361f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4361f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4361f-111">Methods</span></span>

<span data-ttu-id="4361f-112">L'interfaccia **IWpdSerializer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4361f-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="4361f-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="4361f-113">Method</span></span>                                                                                          | <span data-ttu-id="4361f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4361f-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4361f-115">**GetBufferFromIPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4361f-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="4361f-116">Serializza un'interfaccia **IPortableDeviceValues** inviata in una matrice di byte allocata.</span><span class="sxs-lookup"><span data-stu-id="4361f-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="4361f-117">**GetIPortableDeviceValuesFromBuffer**</span><span class="sxs-lookup"><span data-stu-id="4361f-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="4361f-118">Deserializza una matrice di byte in un'interfaccia **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="4361f-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="4361f-119">**GetSerializedSize**</span><span class="sxs-lookup"><span data-stu-id="4361f-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="4361f-120">Calcola la dimensione del buffer necessaria per mantenere un'interfaccia **IPortableDeviceValues** serializzata.</span><span class="sxs-lookup"><span data-stu-id="4361f-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="4361f-121">**WriteIPortableDeviceValuesToBuffer**</span><span class="sxs-lookup"><span data-stu-id="4361f-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="4361f-122">Serializza un'interfaccia **IPortableDeviceValues** in una matrice di byte allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="4361f-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="4361f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4361f-123">Requirements</span></span>



| <span data-ttu-id="4361f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4361f-124">Requirement</span></span> | <span data-ttu-id="4361f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4361f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4361f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4361f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4361f-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4361f-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4361f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="4361f-128">Library</span></span><br/> | <dl> <span data-ttu-id="4361f-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4361f-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4361f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4361f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4361f-131">**Interfacce driver**</span><span class="sxs-lookup"><span data-stu-id="4361f-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 


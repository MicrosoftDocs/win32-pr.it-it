---
title: Interfaccia IWMDRMNetTransmitter
description: L'interfaccia IWMDRMNetTransmitter fornisce i metodi necessari per usare Windows Media DRM per i dispositivi di rete come trasmettitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMNetTransmitter come parametro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Formato Windows Media Interface IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338302"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="a889a-106">Interfaccia IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="a889a-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="a889a-107">L'interfaccia **IWMDRMNetTransmitter** fornisce i metodi necessari per usare Windows Media DRM per i dispositivi di rete come trasmettitore.</span><span class="sxs-lookup"><span data-stu-id="a889a-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="a889a-108">Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="a889a-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="a889a-109">Passare **IID \_ IWMDRMNetTransmitter** come parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="a889a-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="a889a-110">Membri</span><span class="sxs-lookup"><span data-stu-id="a889a-110">Members</span></span>

<span data-ttu-id="a889a-111">L'interfaccia **IWMDRMNetTransmitter** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a889a-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a889a-112">**IWMDRMNetTransmitter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a889a-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="a889a-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a889a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a889a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="a889a-114">Methods</span></span>

<span data-ttu-id="a889a-115">L'interfaccia **IWMDRMNetTransmitter** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a889a-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="a889a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="a889a-116">Method</span></span>                                                                        | <span data-ttu-id="a889a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a889a-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a889a-118">**GetLeafLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="a889a-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="a889a-119">Genera un messaggio di risposta di licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="a889a-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="a889a-120">**GetRootLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="a889a-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="a889a-121">Genera un messaggio di risposta della licenza radice</span><span class="sxs-lookup"><span data-stu-id="a889a-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="a889a-122">**SetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="a889a-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="a889a-123">Elabora una richiesta di licenza inviata da un DRM di Microsoft Windows Media per i dispositivi di rete Receiver</span><span class="sxs-lookup"><span data-stu-id="a889a-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a889a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a889a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a889a-125">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="a889a-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a889a-126">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="a889a-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 


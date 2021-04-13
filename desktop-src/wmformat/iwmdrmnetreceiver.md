---
title: Interfaccia IWMDRMNetReceiver
description: L'interfaccia IWMDRMNetReceiver fornisce i metodi necessari per utilizzare DRM di Microsoft Windows Media per i dispositivi di rete come ricevitore. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMNetReceiver come parametro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Formato Windows Media Interface IWMDRMNetReceiver
- Interfaccia IWMDRMNetReceiver-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398042"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="7c202-106">Interfaccia IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="7c202-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="7c202-107">L'interfaccia **IWMDRMNetReceiver** fornisce i metodi necessari per utilizzare DRM di Microsoft Windows Media per i dispositivi di rete come ricevitore.</span><span class="sxs-lookup"><span data-stu-id="7c202-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="7c202-108">Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="7c202-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="7c202-109">Passare **IID \_ IWMDRMNetReceiver** come parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="7c202-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="7c202-110">Membri</span><span class="sxs-lookup"><span data-stu-id="7c202-110">Members</span></span>

<span data-ttu-id="7c202-111">L'interfaccia **IWMDRMNetReceiver** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="7c202-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="7c202-112">**IWMDRMNetReceiver** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7c202-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="7c202-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="7c202-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c202-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="7c202-114">Methods</span></span>

<span data-ttu-id="7c202-115">L'interfaccia **IWMDRMNetReceiver** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7c202-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="7c202-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="7c202-116">Method</span></span>                                                                               | <span data-ttu-id="7c202-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c202-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c202-118">**GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="7c202-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="7c202-119">Genera un problema di licenza inviato al trasmettitore quando richiede contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="7c202-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="7c202-120">**GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="7c202-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="7c202-121">Genera una richiesta di registrazione inviata al trasmettitore quando il ricevitore si registra o si riconvalida.</span><span class="sxs-lookup"><span data-stu-id="7c202-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="7c202-122">**ProcessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="7c202-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="7c202-123">Elabora la risposta di licenza inviata dalla trasmittente in risposta a una richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="7c202-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="7c202-124">**ProcessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="7c202-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="7c202-125">Elabora la risposta di registrazione inviata dal trasmettitore in risposta a una richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c202-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="7c202-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c202-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c202-127">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="7c202-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7c202-128">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="7c202-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="7c202-129">**Interfaccia IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="7c202-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 






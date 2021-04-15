---
description: Modalità dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modalità dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482701"
---
# <a name="device-mode"></a><span data-ttu-id="fa930-103">Modalità dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa930-103">Device Mode</span></span>

<span data-ttu-id="fa930-104">IEEE 1394 e i camcorder USB possono spostarsi tra la modalità fotocamera e la modalità VTR (video tape recorder).</span><span class="sxs-lookup"><span data-stu-id="fa930-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="fa930-105">Quando una videocamera IEEE 1394 cambia modalità, il dispositivo viene reimpostato e l'applicazione deve enumerarla nuovamente.</span><span class="sxs-lookup"><span data-stu-id="fa930-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="fa930-106">Per un'applicazione non è possibile cambiare la modalità a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="fa930-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="fa930-107">I camcorder USB, d'altra parte, possono passare tra le modalità videocamera e VTR senza reimpostare e l'applicazione può modificare la modalità.</span><span class="sxs-lookup"><span data-stu-id="fa930-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="fa930-108">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="fa930-108">**MSDV Driver**</span></span>

<span data-ttu-id="fa930-109">Per ottenere la modalità corrente su un dispositivo IEEE 1394, chiamare il metodo [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) con il valore del \_ tipo di dispositivo ed DEVCAP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fa930-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="fa930-110">Se il metodo restituisce il valore \_ di ed DEVTYPE \_ VCR, il dispositivo è in modalità VTR e presenta funzioni quali Sospendi, arresta, avanzamento rapido e riavvolgimento.</span><span class="sxs-lookup"><span data-stu-id="fa930-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="fa930-111">In caso contrario, se il metodo restituisce la \_ fotocamera ed DEVTYPE \_ , il dispositivo è in modalità fotocamera.</span><span class="sxs-lookup"><span data-stu-id="fa930-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="fa930-112">Nell'esempio di codice seguente viene illustrato come eseguire una query sul tipo di dispositivo:</span><span class="sxs-lookup"><span data-stu-id="fa930-112">The following code example shows how to query the device type:</span></span>


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



<span data-ttu-id="fa930-113">Se la videocamera passa alla modalità offline, è necessario eseguire di nuovo la query quando diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="fa930-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="fa930-114">Il gestore del grafico dei filtri Invia un evento di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) quando il dispositivo viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="fa930-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="fa930-115">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="fa930-115">**UVC Driver**</span></span>

<span data-ttu-id="fa930-116">Poiché i dispositivi video USB possono cambiare modalità senza reimpostare, il codice illustrato negli esempi precedenti non è affidabile per i dispositivi USB.</span><span class="sxs-lookup"><span data-stu-id="fa930-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="fa930-117">In alternativa, usare l'interfaccia di [**deelezionazione**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) per ottenere la modalità corrente.</span><span class="sxs-lookup"><span data-stu-id="fa930-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="fa930-118">È anche possibile usare questa interfaccia per cambiare le modalità a livello di programmazione se il dispositivo lo supporta.</span><span class="sxs-lookup"><span data-stu-id="fa930-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa930-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa930-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa930-120">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="fa930-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




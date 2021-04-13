---
description: Controllo del volume del decodificatore
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Controllo del volume del decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401314"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="65617-103">Controllo del volume del decodificatore</span><span class="sxs-lookup"><span data-stu-id="65617-103">Decoder Volume Control</span></span>

<span data-ttu-id="65617-104">Le applicazioni controllano il volume audio tramite l'interfaccia [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="65617-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="65617-105">Per KSProxy è disponibile un gestore di interfaccia **IBasicAudio** .</span><span class="sxs-lookup"><span data-stu-id="65617-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="65617-106">Per poter gestire i comandi del volume da KSProxy, un decodificatore deve aggiungere diverse chiavi del registro di sistema nello script di installazione e supportare il set di proprietà **KSPROPSETID \_ Wave** .</span><span class="sxs-lookup"><span data-stu-id="65617-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="65617-107">Creare alcune nuove chiavi del registro di sistema per il driver:</span><span class="sxs-lookup"><span data-stu-id="65617-107">Create some new registry keys for the driver:</span></span>


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



<span data-ttu-id="65617-108">Per implementare il controllo del volume, il driver deve anche supportare **KSPROPSETID \_ Wave**, insieme al volume KsProperty.ID = KsProperty \_ Wave \_ .</span><span class="sxs-lookup"><span data-stu-id="65617-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="65617-109">Questa proprietà viene passata al driver tramite i metodi [**IKsPropertySet:: Get**](ikspropertyset-get.md) e [**IKsPropertySet:: set**](ikspropertyset-set.md) .</span><span class="sxs-lookup"><span data-stu-id="65617-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="65617-110">I campi LeftAttenuation e RightAttentuation specificano i volumi dell'altoparlante sinistro/destro come valori lineari da 0x0000 a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="65617-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65617-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65617-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65617-112">Specifiche e interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="65617-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 




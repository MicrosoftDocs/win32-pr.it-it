---
description: Le classi del dispositivo consentono di specificare le proprietà icons, Label e DeviceHandlers per qualsiasi dispositivo di tale classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando una classe Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994653"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="408ef-103">Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando una classe Device</span><span class="sxs-lookup"><span data-stu-id="408ef-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="408ef-104">Le classi del dispositivo consentono di specificare le proprietà icons, Label e DeviceHandlers per qualsiasi dispositivo di tale classe.</span><span class="sxs-lookup"><span data-stu-id="408ef-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="408ef-105">Questa operazione è simile all'uso dei gruppi di dispositivi, ma le classi di dispositivi e le relative appartenenze sono determinate dall'hardware anziché essere create o assegnate.</span><span class="sxs-lookup"><span data-stu-id="408ef-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="408ef-106">Ogni nome della chiave della classe, che è il GUID dell'interfaccia del dispositivo Plug and Play, si trova sotto la chiave **DeviceClasses** .</span><span class="sxs-lookup"><span data-stu-id="408ef-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="408ef-107">Sotto la singola chiave di classe assegnare i valori per icons, Label e DeviceHandlers.</span><span class="sxs-lookup"><span data-stu-id="408ef-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="408ef-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="408ef-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="408ef-109">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="408ef-109">Step 1:</span></span>

<span data-ttu-id="408ef-110">Nell'esempio seguente vengono illustrati la chiave della classe e i valori DeviceHandlers per l'interfaccia del volume.</span><span class="sxs-lookup"><span data-stu-id="408ef-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

<span data-ttu-id="408ef-111">È anche possibile aggiungere proprietà del dispositivo personalizzate sotto la chiave della classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="408ef-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="408ef-112">Le proprietà personalizzate del dispositivo vengono quindi applicate a tutti i dispositivi di tale classe.</span><span class="sxs-lookup"><span data-stu-id="408ef-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="408ef-113">Ai dispositivi e ai gestori di dispositivi devono essere sempre associate icone ed etichette per soddisfare i requisiti minimi di usabilità.</span><span class="sxs-lookup"><span data-stu-id="408ef-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="408ef-114">Le proprietà definite a livello di istanza del dispositivo hanno la precedenza sulle proprietà definite a livello di gruppo di dispositivi, che a loro volta hanno la precedenza sulle proprietà definite a livello di classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="408ef-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 




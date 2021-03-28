---
description: I gruppi di dispositivi consentono di specificare le proprietà icons, Label o DeviceHandlers per tutti i dispositivi che dichiarano parte di tale gruppo.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando un gruppo di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967440"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="21e84-103">Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando un gruppo di dispositivi</span><span class="sxs-lookup"><span data-stu-id="21e84-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="21e84-104">I gruppi di dispositivi consentono di specificare le proprietà icons, Label o DeviceHandlers per tutti i dispositivi che dichiarano parte di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="21e84-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="21e84-105">Se il gruppo di dispositivi non è un gruppo di dispositivi fornito dal sistema, una chiave che definisce il gruppo di dispositivi verrà aggiunta sotto la \\ chiave **DeviceGroups** di AutoplayHandlers.</span><span class="sxs-lookup"><span data-stu-id="21e84-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="21e84-106">Non è necessario impostare tutte e tre le proprietà per ogni gruppo. è possibile impostare solo le proprietà che si desidera personalizzare.</span><span class="sxs-lookup"><span data-stu-id="21e84-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="21e84-107">Tuttavia, i dispositivi e i gestori di dispositivi devono avere sempre le icone e le etichette associate per soddisfare i requisiti minimi di usabilità.</span><span class="sxs-lookup"><span data-stu-id="21e84-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="21e84-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="21e84-108">Instructions</span></span>


<span data-ttu-id="21e84-109">Nell'esempio seguente viene utilizzato un sistema con diverse unità zip collegate.</span><span class="sxs-lookup"><span data-stu-id="21e84-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="21e84-110">Se non si specificano i valori Icon, Label e DeviceHandlers per ogni unità singolarmente, viene creato un gruppo di dispositivi denominato ZipDrive e tali valori vengono definiti al suo interno.</span><span class="sxs-lookup"><span data-stu-id="21e84-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="21e84-111">Ogni unità zip viene quindi dichiarata come membro del gruppo ZipDrive.</span><span class="sxs-lookup"><span data-stu-id="21e84-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="21e84-112">Per prima cosa, definire il gruppo di dispositivi aggiungendo la chiave *ZipDrive* seguente e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="21e84-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

<span data-ttu-id="21e84-113">Ogni dispositivo di unità zip viene quindi dichiarato come parte del gruppo ZipDrive, ereditando le proprietà di tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="21e84-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="21e84-114">Nella chiave **DeviceParameters** dell'istanza del dispositivo aggiungere un valore denominato gruppo come tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="21e84-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="21e84-115">L'immissione di dati per questo valore è il nome del gruppo di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="21e84-115">The data entry for this value is the name of the device group.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

<span data-ttu-id="21e84-116">È anche possibile aggiungere proprietà del dispositivo personalizzate diverse dalle icone, etichetta e DeviceHandlers sotto la chiave del gruppo di dispositivi e quindi applicarle a tutti i dispositivi che appartengono a tale gruppo di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="21e84-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="21e84-117">Le proprietà definite a livello di istanza del dispositivo hanno la precedenza sulle proprietà definite a livello di gruppo di dispositivi, che a loro volta hanno la precedenza sulle proprietà definite a livello di classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21e84-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 




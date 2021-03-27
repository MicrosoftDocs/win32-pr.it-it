---
description: Viene illustrato il processo per l'aggiunta di un gestore di dispositivo a un dispositivo.
title: Come assegnare un gestore di dispositivo a un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979615"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="3da65-103">Come assegnare un gestore di dispositivo a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="3da65-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="3da65-104">Viene illustrato il processo per l'aggiunta di un gestore di dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3da65-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="3da65-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="3da65-105">Instructions</span></span>


<span data-ttu-id="3da65-106">Per assegnare un gestore di dispositivo a un dispositivo, nella sottochiave **parametri dispositivo** dell'istanza del dispositivo aggiungere un valore di tipo **reg \_ SZ** denominato **DeviceHandlers**.</span><span class="sxs-lookup"><span data-stu-id="3da65-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="3da65-107">L'immissione di dati per questo valore è il nome del gestore di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3da65-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="3da65-108">Di seguito è riportata una voce di esempio per un dispositivo vid 0031 fittizio \_ 059&PID \_ .</span><span class="sxs-lookup"><span data-stu-id="3da65-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

<span data-ttu-id="3da65-109">I gestori di dispositivo possono anche essere assegnati usando le impostazioni di [gruppo di dispositivi](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) o di [dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3da65-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 




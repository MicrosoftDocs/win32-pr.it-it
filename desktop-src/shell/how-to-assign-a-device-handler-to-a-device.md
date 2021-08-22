---
description: Illustra il processo per l'aggiunta di un gestore del dispositivo a un dispositivo.
title: Come assegnare un gestore di dispositivo a un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092975"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Come assegnare un gestore di dispositivo a un dispositivo

Illustra il processo per l'aggiunta di un gestore del dispositivo a un dispositivo.

## <a name="instructions"></a>Istruzioni


Per assegnare un gestore di dispositivi a un dispositivo, nella sottochiave **Device Parameters** dell'istanza del dispositivo aggiungere un valore di tipo **REG \_ SZ** denominato **DeviceHandlers.** La voce di dati per questo valore è il nome del gestore del dispositivo.

Di seguito è riportato un esempio di voce per un dispositivo Fittizio Vid \_ 059&\_ Pid 0031.

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

I gestori di dispositivi possono essere assegnati anche usando le [impostazioni del gruppo di dispositivi](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) o della classe [di](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) dispositivi.

 

 




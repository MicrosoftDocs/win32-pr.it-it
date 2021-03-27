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
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Come assegnare un gestore di dispositivo a un dispositivo

Viene illustrato il processo per l'aggiunta di un gestore di dispositivo a un dispositivo.

## <a name="instructions"></a>Istruzioni


Per assegnare un gestore di dispositivo a un dispositivo, nella sottochiave **parametri dispositivo** dell'istanza del dispositivo aggiungere un valore di tipo **reg \_ SZ** denominato **DeviceHandlers**. L'immissione di dati per questo valore è il nome del gestore di dispositivo.

Di seguito è riportata una voce di esempio per un dispositivo vid 0031 fittizio \_ 059&PID \_ .

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

I gestori di dispositivo possono anche essere assegnati usando le impostazioni di [gruppo di dispositivi](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) o di [dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .

 

 




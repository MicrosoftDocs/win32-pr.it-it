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
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando un gruppo di dispositivi

I gruppi di dispositivi consentono di specificare le proprietà icons, Label o DeviceHandlers per tutti i dispositivi che dichiarano parte di tale gruppo. Se il gruppo di dispositivi non è un gruppo di dispositivi fornito dal sistema, una chiave che definisce il gruppo di dispositivi verrà aggiunta sotto la \\ chiave **DeviceGroups** di AutoplayHandlers. Non è necessario impostare tutte e tre le proprietà per ogni gruppo. è possibile impostare solo le proprietà che si desidera personalizzare. Tuttavia, i dispositivi e i gestori di dispositivi devono avere sempre le icone e le etichette associate per soddisfare i requisiti minimi di usabilità.

## <a name="instructions"></a>Istruzioni


Nell'esempio seguente viene utilizzato un sistema con diverse unità zip collegate. Se non si specificano i valori Icon, Label e DeviceHandlers per ogni unità singolarmente, viene creato un gruppo di dispositivi denominato ZipDrive e tali valori vengono definiti al suo interno. Ogni unità zip viene quindi dichiarata come membro del gruppo ZipDrive.

Per prima cosa, definire il gruppo di dispositivi aggiungendo la chiave *ZipDrive* seguente e i relativi valori.

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

Ogni dispositivo di unità zip viene quindi dichiarato come parte del gruppo ZipDrive, ereditando le proprietà di tale gruppo. Nella chiave **DeviceParameters** dell'istanza del dispositivo aggiungere un valore denominato gruppo come tipo **reg \_ SZ**. L'immissione di dati per questo valore è il nome del gruppo di dispositivi.

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

È anche possibile aggiungere proprietà del dispositivo personalizzate diverse dalle icone, etichetta e DeviceHandlers sotto la chiave del gruppo di dispositivi e quindi applicarle a tutti i dispositivi che appartengono a tale gruppo di dispositivi.

> [!Note]  
> Le proprietà definite a livello di istanza del dispositivo hanno la precedenza sulle proprietà definite a livello di gruppo di dispositivi, che a loro volta hanno la precedenza sulle proprietà definite a livello di classe del dispositivo.

 

 

 




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
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando una classe Device

Le classi del dispositivo consentono di specificare le proprietà icons, Label e DeviceHandlers per qualsiasi dispositivo di tale classe. Questa operazione è simile all'uso dei gruppi di dispositivi, ma le classi di dispositivi e le relative appartenenze sono determinate dall'hardware anziché essere create o assegnate. Ogni nome della chiave della classe, che è il GUID dell'interfaccia del dispositivo Plug and Play, si trova sotto la chiave **DeviceClasses** . Sotto la singola chiave di classe assegnare i valori per icons, Label e DeviceHandlers.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Nell'esempio seguente vengono illustrati la chiave della classe e i valori DeviceHandlers per l'interfaccia del volume.

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

È anche possibile aggiungere proprietà del dispositivo personalizzate sotto la chiave della classe del dispositivo. Le proprietà personalizzate del dispositivo vengono quindi applicate a tutti i dispositivi di tale classe. Ai dispositivi e ai gestori di dispositivi devono essere sempre associate icone ed etichette per soddisfare i requisiti minimi di usabilità.

> [!Note]  
> Le proprietà definite a livello di istanza del dispositivo hanno la precedenza sulle proprietà definite a livello di gruppo di dispositivi, che a loro volta hanno la precedenza sulle proprietà definite a livello di classe del dispositivo.

 

 

 




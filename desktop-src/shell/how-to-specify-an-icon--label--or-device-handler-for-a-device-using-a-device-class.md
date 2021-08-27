---
description: Le classi di dispositivi consentono di specificare le proprietà Icons, Label e DeviceHandlers per qualsiasi dispositivo di tale classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Come specificare un'icona, un'etichetta o un gestore di dispositivi per un dispositivo usando una classe di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ef06228d9b533f2793384c0053017f06aca72d05bd64c5333aa2aadca48dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111771"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Come specificare un'icona, un'etichetta o un gestore di dispositivi per un dispositivo usando una classe di dispositivi

Le classi di dispositivi consentono di specificare le proprietà Icons, Label e DeviceHandlers per qualsiasi dispositivo di tale classe. Questo è simile all'uso dei gruppi di dispositivi, ma le classi di dispositivi e le relative appartenenze sono determinate dall'hardware anziché essere create o assegnate. Ogni nome di chiave di classe, che Plug and Play GUID dell'interfaccia del dispositivo, si trova sotto la **chiave DeviceClasses.** Nella chiave della singola classe assegnare i valori per Icons, Label e DeviceHandlers.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

L'esempio seguente mostra la chiave della classe e i valori DeviceHandlers per l'interfaccia del volume.

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

È anche possibile aggiungere proprietà personalizzate del dispositivo sotto la chiave della classe del dispositivo. Le proprietà personalizzate del dispositivo vengono quindi applicate a tutti i dispositivi nella classe. I dispositivi e i gestori di dispositivi devono sempre avere icone ed etichette associate per soddisfare i requisiti minimi di usabilità.

> [!Note]  
> Le proprietà definite a livello di istanza del dispositivo hanno la precedenza sulle proprietà definite a livello di gruppo di dispositivi, che a loro volta hanno la precedenza sulle proprietà definite a livello di classe di dispositivo.

 

 

 




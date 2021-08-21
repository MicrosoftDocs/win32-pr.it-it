---
description: Controllo volume decodificatore
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Controllo volume decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e96ed9efb17a4fb32c41d8b10313edbe015c202b7f7d1f4287e1af20cca559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953150"
---
# <a name="decoder-volume-control"></a>Controllo volume decodificatore

Le applicazioni controllano il volume audio tramite [**l'interfaccia IBasicAudio.**](/windows/desktop/api/Control/nn-control-ibasicaudio) Per KSProxy viene fornito un gestore di interfaccia **IBasicAudio.** Per gestire i comandi del volume da KSProxy, un decodificatore deve aggiungere diverse chiavi del Registro di sistema nello script di installazione e supportare il set di proprietà **Wave KSPROPSETID. \_**

Creare alcune nuove chiavi del Registro di sistema per il driver:


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



Per implementare il controllo del volume, il driver deve anche supportare **KSPROPSETID \_ Wave**, insieme KsProperty.Id = KSPROPERTY \_ WAVE \_ VOLUME. Questa proprietà viene passata al driver tramite i [**metodi IKsPropertySet::Get**](ikspropertyset-get.md) [**e IKsPropertySet::Set.**](ikspropertyset-set.md) I campi LeftAttenuation e RightAttentuation specificano i volumi della voce sinistra/destra come valori lineari da 0x0000 a 0xffff.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce e specifiche del decodificatore](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 




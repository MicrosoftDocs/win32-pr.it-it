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
# <a name="decoder-volume-control"></a>Controllo del volume del decodificatore

Le applicazioni controllano il volume audio tramite l'interfaccia [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) . Per KSProxy è disponibile un gestore di interfaccia **IBasicAudio** . Per poter gestire i comandi del volume da KSProxy, un decodificatore deve aggiungere diverse chiavi del registro di sistema nello script di installazione e supportare il set di proprietà **KSPROPSETID \_ Wave** .

Creare alcune nuove chiavi del registro di sistema per il driver:


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



Per implementare il controllo del volume, il driver deve anche supportare **KSPROPSETID \_ Wave**, insieme al volume KsProperty.ID = KsProperty \_ Wave \_ . Questa proprietà viene passata al driver tramite i metodi [**IKsPropertySet:: Get**](ikspropertyset-get.md) e [**IKsPropertySet:: set**](ikspropertyset-set.md) . I campi LeftAttenuation e RightAttentuation specificano i volumi dell'altoparlante sinistro/destro come valori lineari da 0x0000 a 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifiche e interfacce del decodificatore](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 




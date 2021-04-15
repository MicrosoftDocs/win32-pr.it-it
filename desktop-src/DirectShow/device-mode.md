---
description: Modalità dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modalità dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482701"
---
# <a name="device-mode"></a>Modalità dispositivo

IEEE 1394 e i camcorder USB possono spostarsi tra la modalità fotocamera e la modalità VTR (video tape recorder). Quando una videocamera IEEE 1394 cambia modalità, il dispositivo viene reimpostato e l'applicazione deve enumerarla nuovamente. Per un'applicazione non è possibile cambiare la modalità a livello di codice. I camcorder USB, d'altra parte, possono passare tra le modalità videocamera e VTR senza reimpostare e l'applicazione può modificare la modalità.

**Driver MSDV**

Per ottenere la modalità corrente su un dispositivo IEEE 1394, chiamare il metodo [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) con il valore del \_ tipo di dispositivo ed DEVCAP \_ \_ . Se il metodo restituisce il valore \_ di ed DEVTYPE \_ VCR, il dispositivo è in modalità VTR e presenta funzioni quali Sospendi, arresta, avanzamento rapido e riavvolgimento. In caso contrario, se il metodo restituisce la \_ fotocamera ed DEVTYPE \_ , il dispositivo è in modalità fotocamera. Nell'esempio di codice seguente viene illustrato come eseguire una query sul tipo di dispositivo:


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



Se la videocamera passa alla modalità offline, è necessario eseguire di nuovo la query quando diventa disponibile. Il gestore del grafico dei filtri Invia un evento di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) quando il dispositivo viene rimosso.

**Driver UVC**

Poiché i dispositivi video USB possono cambiare modalità senza reimpostare, il codice illustrato negli esempi precedenti non è affidabile per i dispositivi USB. In alternativa, usare l'interfaccia di [**deelezionazione**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) per ottenere la modalità corrente. È anche possibile usare questa interfaccia per cambiare le modalità a livello di programmazione se il dispositivo lo supporta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




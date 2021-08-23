---
description: 'Altre informazioni su: Connessione a un dispositivo'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Connessione a un dispositivo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451221"
---
# <a name="connecting-to-a-device"></a>Connessione a un dispositivo

> [!Note]  
> Questo sistema di scripting è stato sostituito con Windows di automazione wia (Image Acquisition). Vedere [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Il primo passaggio in qualsiasi applicazione o script che usa il modello di scripting Windows Image Acquisition (WIA) consiste nella creazione [**dell'oggetto Wia.**](-wia-wia.md) Questo oggetto fornisce metodi per ottenere una raccolta di [**oggetti DeviceInfo**](-wia-deviceinfo.md) e connettere tali oggetti ai dispositivi. Offre anche la possibilità di restare in ascolto di eventi hardware WIA.

La riga di codice Microsoft Visual Basic Scripting Edition (VBScript) seguente crea [**l'oggetto Wia:**](-wia-wia.md)


```
objWia = CreateObject("Wia.Script")
```



Dopo aver creato [**l'oggetto Wia,**](-wia-wia.md) usare [**il metodo Create**](-wia-iwia-create.md) per connettersi a un dispositivo hardware WIA.

È anche possibile usare la proprietà [**Devices**](-wia-iwia-devices.md) dell'oggetto [**Wia**](-wia-wia.md) per ottenere una raccolta di [**oggetti DeviceInfo.**](-wia-deviceinfo.md) Enumerare questa raccolta e usare [**il metodo Create**](-wia-iwiadeviceinfo-create.md) per connettersi a un dispositivo.

 

 

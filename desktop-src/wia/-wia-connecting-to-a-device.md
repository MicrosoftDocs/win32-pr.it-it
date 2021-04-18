---
description: 'Altre informazioni su: connessione a un dispositivo'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Connessione a un dispositivo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312450"
---
# <a name="connecting-to-a-device"></a>Connessione a un dispositivo

> [!Note]  
> Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA). Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Il primo passaggio in qualsiasi applicazione o script che utilizza il modello di scripting Windows Image Acquisition (WIA) consiste nel creare l'oggetto [**WIA**](-wia-wia.md) . Questo oggetto fornisce i metodi per ottenere una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) e connettere questi oggetti ai dispositivi. Offre inoltre la possibilità di restare in ascolto degli eventi hardware WIA.

La seguente riga di codice Microsoft Visual Basic Scripting Edition (VBScript) crea l'oggetto [**WIA**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Dopo aver creato l'oggetto [**WIA**](-wia-wia.md) , utilizzare il relativo metodo [**create**](-wia-iwia-create.md) per connettersi a un dispositivo hardware WIA.

È anche possibile usare la proprietà [**Devices**](-wia-iwia-devices.md) dell'oggetto [**WIA**](-wia-wia.md) per ottenere una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) . Enumerare questa raccolta e usare il metodo [**create**](-wia-iwiadeviceinfo-create.md) per connettersi a un dispositivo.

 

 

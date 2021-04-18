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
# <a name="connecting-to-a-device"></a><span data-ttu-id="bdefd-103">Connessione a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdefd-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="bdefd-104">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="bdefd-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="bdefd-105">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="bdefd-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="bdefd-106">Il primo passaggio in qualsiasi applicazione o script che utilizza il modello di scripting Windows Image Acquisition (WIA) consiste nel creare l'oggetto [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="bdefd-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="bdefd-107">Questo oggetto fornisce i metodi per ottenere una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) e connettere questi oggetti ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="bdefd-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="bdefd-108">Offre inoltre la possibilità di restare in ascolto degli eventi hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="bdefd-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="bdefd-109">La seguente riga di codice Microsoft Visual Basic Scripting Edition (VBScript) crea l'oggetto [**WIA**](-wia-wia.md) :</span><span class="sxs-lookup"><span data-stu-id="bdefd-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="bdefd-110">Dopo aver creato l'oggetto [**WIA**](-wia-wia.md) , utilizzare il relativo metodo [**create**](-wia-iwia-create.md) per connettersi a un dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="bdefd-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="bdefd-111">È anche possibile usare la proprietà [**Devices**](-wia-iwia-devices.md) dell'oggetto [**WIA**](-wia-wia.md) per ottenere una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bdefd-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="bdefd-112">Enumerare questa raccolta e usare il metodo [**create**](-wia-iwiadeviceinfo-create.md) per connettersi a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdefd-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 

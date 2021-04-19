---
description: Una raccolta è un oggetto che contiene uno o più oggetti. Le raccolte consentono di raggruppare in modo efficiente oggetti simili. Windows Image Acquisition (WIA) fornisce raccolte per gli oggetti DeviceInfo e Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Utilizzo di oggetti Collection WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307323"
---
# <a name="using-wia-collection-objects"></a><span data-ttu-id="2100b-105">Utilizzo di oggetti Collection WIA</span><span class="sxs-lookup"><span data-stu-id="2100b-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="2100b-106">Una raccolta è un oggetto che contiene uno o più oggetti.</span><span class="sxs-lookup"><span data-stu-id="2100b-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="2100b-107">Le raccolte consentono di raggruppare in modo efficiente oggetti simili.</span><span class="sxs-lookup"><span data-stu-id="2100b-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="2100b-108">Windows Image Acquisition (WIA) fornisce raccolte per gli oggetti [**deviceInfo**](-wia-deviceinfo.md) e [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2100b-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="2100b-109">Usare le raccolte per enumerare gli oggetti in essi contenuti.</span><span class="sxs-lookup"><span data-stu-id="2100b-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="2100b-110">Ad esempio, l'esempio VBScript seguente ottiene una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) dal metodo [**Devices**](-wia-iwia-devices.md) e quindi usa un **per... Ogni** ciclo per scorrere la raccolta:</span><span class="sxs-lookup"><span data-stu-id="2100b-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> <span data-ttu-id="2100b-111">Gli oggetti Collection WIA sono basati su 0.</span><span class="sxs-lookup"><span data-stu-id="2100b-111">WIA collection objects are 0-based.</span></span>

 

 

 




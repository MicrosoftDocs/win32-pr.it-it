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
# <a name="using-wia-collection-objects"></a>Utilizzo di oggetti Collection WIA

Una raccolta è un oggetto che contiene uno o più oggetti. Le raccolte consentono di raggruppare in modo efficiente oggetti simili. Windows Image Acquisition (WIA) fornisce raccolte per gli oggetti [**deviceInfo**](-wia-deviceinfo.md) e [**Item**](-wia-item.md) .

Usare le raccolte per enumerare gli oggetti in essi contenuti. Ad esempio, l'esempio VBScript seguente ottiene una raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) dal metodo [**Devices**](-wia-iwia-devices.md) e quindi usa un **per... Ogni** ciclo per scorrere la raccolta:


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
> Gli oggetti Collection WIA sono basati su 0.

 

 

 




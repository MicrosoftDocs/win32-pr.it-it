---
description: Windows Acquisizione di immagini (WIA) fornisce oggetti di automazione da usare nei linguaggi di scripting, ad esempio microsoft JScript e software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio il sistema di sviluppo Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modello di scripting WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b558e84dd4095fd0d5dc3f1f14a7de76d9108c488cf3fc3613e3a09bc4830714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812851"
---
# <a name="wia-scripting-model"></a>Modello di scripting WIA

Windows Acquisizione di immagini (WIA) fornisce oggetti di automazione da usare nei linguaggi di scripting, ad esempio microsoft JScript e software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio il sistema di sviluppo Microsoft Visual Basic.

> [!Note]  
> Questo sistema di scripting è stato sostituito con Windows di automazione di acquisizione di immagini (WIA). Vedere [Windows di automazione dell'acquisizione di immagini.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

La tabella seguente descrive gli oggetti di scripting WIA e come vengono usati. 

| Oggetto                                | Descrizione                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wia**](-wia-wia.md)               | Oggetto di scripting WIA di primo livello. Usare [**l'oggetto Wia**](-wia-wia.md) per enumerare e connettersi ai dispositivi e per gestire gli eventi dei dispositivi hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | [**L'oggetto DeviceInfo**](-wia-deviceinfo.md) fornisce l'accesso alle informazioni sulle proprietà del dispositivo.                                                                                     |
| [**Elemento**](-wia-item.md)             | Questo oggetto rappresenta gli elementi del dispositivo, del file e della cartella WIA. Un dispositivo hardware WIA e le relative immagini o letti da scansione sono rappresentati come un albero gerarchico di [**oggetti Item.**](-wia-item.md) |



 

Sia [**l'oggetto DeviceInfo**](-wia-deviceinfo.md) che [**l'oggetto Item**](-wia-item.md) sono associati a oggetti raccolta. Per informazioni sull'uso degli oggetti raccolta, vedere Using WIA Collection Objects.

Negli argomenti seguenti vengono fornite informazioni generali sull'uso del modello di scripting WIA:

-   [Convenzioni della sintassi](-wia-syntax-conventions.md)
-   [Uso di oggetti raccolta WIA](-wia-using-wia-collection-objects.md)
-   [Definizioni delle costanti delle proprietà WIA](-wia-wia-property-constant-definitions.md)

 

 

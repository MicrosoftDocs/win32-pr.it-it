---
description: Windows Image Acquisition (WIA) fornisce oggetti di automazione da utilizzare nei linguaggi di scripting, ad esempio Microsoft JScript e il software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio Microsoft Visual Basic Development System.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modello di scripting WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307306"
---
# <a name="wia-scripting-model"></a>Modello di scripting WIA

Windows Image Acquisition (WIA) fornisce oggetti di automazione da utilizzare nei linguaggi di scripting, ad esempio Microsoft JScript e il software di sviluppo Microsoft Visual Basic Scripting Edition (VBScript) e linguaggi di programmazione di alto livello, ad esempio Microsoft Visual Basic Development System.

> [!Note]  
> Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA). Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Nella tabella seguente vengono descritti gli oggetti di scripting WIA e il modo in cui vengono utilizzati. 

| Oggetto                                | Descrizione                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WIA**](-wia-wia.md)               | Oggetto di scripting WIA di primo livello. Usare l'oggetto [**WIA**](-wia-wia.md) per enumerare e connettersi ai dispositivi e per gestire gli eventi del dispositivo hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | L'oggetto [**deviceInfo**](-wia-deviceinfo.md) fornisce l'accesso alle informazioni sulle proprietà del dispositivo.                                                                                     |
| [**Elemento**](-wia-item.md)             | Questo oggetto rappresenta gli elementi WIA del dispositivo, del file e della cartella. Un dispositivo hardware WIA, le relative immagini o i letti di analisi sono rappresentati come albero gerarchico di oggetti [**elemento**](-wia-item.md) . |



 

Sia l'oggetto [**deviceInfo**](-wia-deviceinfo.md) che l'oggetto [**Item**](-wia-item.md) sono associati agli oggetti della raccolta. Per informazioni sull'utilizzo di oggetti Collection, vedere Using WIA Collection Objects.

Negli argomenti seguenti vengono illustrate le informazioni generali sull'utilizzo del modello di scripting WIA:

-   [Convenzioni della sintassi](-wia-syntax-conventions.md)
-   [Utilizzo di oggetti Collection WIA](-wia-using-wia-collection-objects.md)
-   [Definizioni di costanti della proprietà WIA](-wia-wia-property-constant-definitions.md)

 

 

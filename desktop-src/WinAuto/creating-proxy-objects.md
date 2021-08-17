---
title: Creazione di oggetti proxy
description: Oltre a progettare classi che implementano proprietà e metodi IAccessible, gli sviluppatori di server possono anche dover progettare oggetti proxy che monitorano l'intervallo di vita degli oggetti accessibili.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133894"
---
# <a name="creating-proxy-objects"></a>Creazione di oggetti proxy

Oltre a progettare classi che implementano proprietà e metodi [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) gli sviluppatori di server possono anche dover progettare oggetti *proxy* che monitorano l'intervallo di vita degli oggetti accessibili. Se un oggetto accessibile in un'applicazione è disponibile per l'intera esecuzione dell'applicazione, non è necessario creare un oggetto proxy. Se è possibile eliminare l'oggetto accessibile mentre l'applicazione è in esecuzione, è necessario creare un oggetto proxy.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Che cosa sono gli oggetti proxy?](what-are-proxy-objects.md)
-   [Perché sono necessari oggetti proxy](why-proxy-objects-are-needed.md)
-   [Considerazioni sulla progettazione per gli oggetti proxy](design-considerations-for-proxy-objects.md)

 

 





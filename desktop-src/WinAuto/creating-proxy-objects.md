---
title: Creazione di oggetti proxy
description: Oltre a progettare classi che implementano proprietà e metodi IAccessible, gli sviluppatori di server possono anche progettare oggetti proxy che monitorano la durata degli oggetti accessibili.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708554"
---
# <a name="creating-proxy-objects"></a>Creazione di oggetti proxy

Oltre a progettare classi che implementano proprietà e metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , gli sviluppatori di server possono anche progettare oggetti *proxy* che monitorano la durata degli oggetti accessibili. Se un oggetto accessibile in un'applicazione è disponibile per tutto il tempo in cui l'applicazione è in esecuzione, non è necessario creare un oggetto proxy. Se è possibile eliminare l'oggetto accessibile mentre l'applicazione è in esecuzione, è necessario creare un oggetto proxy.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Che cosa sono gli oggetti proxy?](what-are-proxy-objects.md)
-   [Perché gli oggetti proxy sono necessari](why-proxy-objects-are-needed.md)
-   [Considerazioni di progettazione per gli oggetti proxy](design-considerations-for-proxy-objects.md)

 

 





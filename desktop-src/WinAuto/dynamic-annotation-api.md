---
title: API di annotazione dinamica
description: L'API di annotazione dinamica è un'estensione di Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto di IAccessible esistente senza dover utilizzare tecniche di sottoclasse o di wrapping soggette a errori.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955844"
---
# <a name="dynamic-annotation-api"></a>API di annotazione dinamica

L'API di annotazione dinamica è un'estensione di Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente senza dover utilizzare tecniche di sottoclasse o di wrapping soggette a errori. Questo meccanismo consente inoltre agli sviluppatori di passare suggerimenti o altre informazioni utili ai proxy Oleacc.dll.

L'annotazione dinamica viene in genere usata per correggere o modificare un'istanza non corretta di un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esposto da un proxy di Oleacc.dll esistente. Ad esempio, è possibile usarlo per eseguire l'override delle proprietà [**Name**](name-property.md) e [**Role**](role-property.md) fornite dal proxy predefinito e per fornire la [**Descrizione**](description-property.md) e le proprietà della [**Guida**](help-property.md) (che potrebbero non essere fornite dal proxy predefinito).

Con Windows 7, gli sviluppatori possono usare l'API di annotazione dinamica per annotare le proprietà di automazione interfaccia utente Microsoft, nonché le proprietà di Microsoft Active Accessibility degli oggetti proxy creati da Oleacc.dll per i controlli Windows standard. Gli oggetti proxy Oleacc.dll servono sia Microsoft Active Accessibility che client di automazione interfaccia utente.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Informazioni di base](background-information.md)
-   [Alternative all'annotazione dinamica](alternatives-to-dynamic-annotation.md)
-   [Tipi di annotazione dinamica](types-of-dynamic-annotation.md)
-   [Annotazione diretta](direct-annotation.md)
-   [Annotazione mappa valori](value-map-annotation.md)
-   [Annotazione server](server-annotation.md)
-   [Problemi e limitazioni](issues-and-limitations.md)

 

 





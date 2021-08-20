---
title: API di annotazione dinamica
description: L'API Di annotazione dinamica è un'estensione Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto IAccessible esistente senza dover usare tecniche di creazione di sottoclassi o wrapping erre.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8b95d1175d4a6bd894e79c55f6798a73165fab2d6e6da40e3b952e68824d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115321"
---
# <a name="dynamic-annotation-api"></a>API di annotazione dinamica

L'API Di annotazione dinamica è un'estensione per Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente senza dover usare tecniche di creazione di sottoclassi o wrapping erre. Questo meccanismo consente inoltre agli sviluppatori di passare hint o altre informazioni utili ai proxy Oleacc.dll proxy.

L'annotazione dinamica viene in genere usata per correggere o modificare un'istanza non corretta di un [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esposto da un proxy Oleacc.dll esistente. Ad esempio, è possibile usarlo per eseguire l'override delle proprietà [**Name**](name-property.md) e [**Role**](role-property.md) fornite dal proxy predefinito e per fornire le proprietà [**Description**](description-property.md) e [**Help**](help-property.md) (che potrebbero non essere fornite dal proxy predefinito).

Con Windows 7, gli sviluppatori possono usare l'API Di annotazione dinamica per annotare le proprietà di Microsoft Automazione interfaccia utente e le proprietà Microsoft Active Accessibility degli oggetti proxy creati da Oleacc.dll per i controlli Windows standard. Gli Oleacc.dll proxy vengono utilizzati sia Microsoft Active Accessibility che Automazione interfaccia utente client.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Informazioni di base](background-information.md)
-   [Alternative all'annotazione dinamica](alternatives-to-dynamic-annotation.md)
-   [Tipi di annotazione dinamica](types-of-dynamic-annotation.md)
-   [Annotazione diretta](direct-annotation.md)
-   [Annotazione mappa valori](value-map-annotation.md)
-   [Annotazione server](server-annotation.md)
-   [Problemi e limitazioni](issues-and-limitations.md)

 

 





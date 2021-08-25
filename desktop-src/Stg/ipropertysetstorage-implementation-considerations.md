---
title: Considerazioni sull'implementazione di IPropertySetStorage
description: Quando si valuta come fornire un'implementazione dell'interfaccia IPropertySetStorage che legge e scrive il formato del set di proprietà COM, si verificano diversi problemi. Le sezioni seguenti descrivono queste considerazioni.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c74800eb0721d881825d48781ac0f3dd2517e0beeb86077312e3ad8c8cbe9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961341"
---
# <a name="ipropertysetstorage-implementation-considerations"></a>Considerazioni sull'implementazione di IPropertySetStorage

Quando si valuta come fornire un'implementazione [**dell'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) che legge e scrive il formato del set di proprietà COM, si verificano diversi problemi. Le sezioni seguenti descrivono queste considerazioni.

-   [Nomi in IStorage](names-in-istorage.md)
-   [Archiviazione e oggetti Stream per un set di proprietà](storage-vs--stream-for-a-property-set.md)
-   [Impostazione dell'identificatore di classe del set di proprietà](setting-the-property-set-class-identifier.md)
-   [Punti di sincronizzazione](synchronization-points.md)
-   [Code Pages e stringhe Unicode](code-pages-and-unicode-strings.md)
-   [Dizionario](dictionary.md)
-   [Estensioni](extensions.md)
-   [Serializzazione del set di proprietà](version-0-vs--version-1-property-set-serialization.md)

Per altre informazioni, vedere [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) nella sezione Riferimento in Interfacce.

 

 





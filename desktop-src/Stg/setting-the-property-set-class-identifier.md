---
title: Impostazione dell'identificatore di classe del set di proprietà
description: Il Metodo IPropertyStorage della classe imposta sia il CLSID dell'oggetto di archiviazione che il valore del tag di classe archiviato nel set di proprietà COM. Questo errore si verifica quando viene richiamato su un archivio di proprietà non semplice archiviato in un oggetto di archiviazione strutturato.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Impostazione dell'identificatore di classe del set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045155"
---
# <a name="setting-the-property-set-class-identifier"></a>Impostazione dell'identificatore di classe del set di proprietà

Il metodo [**IPropertyStorage::**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) SetProperty imposta sia il CLSID dell'oggetto di archiviazione che il valore del tag di classe archiviato nel set di proprietà com. Questo errore si verifica quando viene richiamato su un archivio di proprietà non semplice archiviato in un oggetto di archiviazione strutturato.

In questo modo si garantisce coerenza e uniformità che consente di migliorare l'interazione con alcuni strumenti. Un oggetto di archiviazione delle proprietà non è semplice se viene creato chiamando [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con il flag **PROPSETFLAG non \_ semplice** impostato.

Il CLSID dell'oggetto di archiviazione viene impostato con una chiamata a [**IStorage:: seclass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).

 

 





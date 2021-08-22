---
title: Archiviazione e oggetti Stream per un set di proprietà
description: Il programmatore specifica se un set di proprietà viene archiviato in un archivio o in un flusso quando viene creato il set di proprietà.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661841"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Archiviazione e oggetti Stream per un set di proprietà

Il programmatore specifica se un set di proprietà viene archiviato in un archivio o in un flusso quando viene creato il set di proprietà. Il valore di enumerazione PROPSETFLAG NONSIMPLE, passato nel parametro \_ *grfFlags* al metodo [**IPropertySetStorage::Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) indica questo valore. L'impostazione della posizione in cui è archiviato il set di proprietà fornisce controlli dell'applicazione adeguati per l'interoperabilità completa tramite [**l'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) con il set di proprietà COM.

Se il flag PROPSETFLAG NONSIMPLE è impostato, il set di proprietà viene archiviato in un oggetto di archiviazione e possono essere scritti valori di proprietà \_ nonsimple. I valori non disimple includono valori con **VARTYPE** di VT \_ STORAGE, VT \_ STREAM, VT \_ STORED OBJECT o \_ VT \_ STREAMED \_ OBJECT. Per altre informazioni sui **valori VARTYPE** e su come usarli, vedere la [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Se il flag PROPSETFLAG NONSIMPLE non è impostato, nel set di proprietà possono essere scritti solo \_ valori semplici.

Nell'oggetto di archiviazione di un set di proprietà nonsimple viene creato un flusso denominato Contents. Si tratta del flusso primario del set di proprietà e contiene tutti i valori di proprietà semplici. I valori delle proprietà non di base (flussi e archivi) vengono archiviati nell'oggetto di archiviazione principale del set di proprietà come flussi secondari e archivi. In altri casi, questi valori non semplici vengono archiviati come elementi di pari livello nel flusso Contents. Il nome dei flussi e delle risorse di archiviazione di pari livello è determinato dall'implementazione e archiviato nel flusso Contents in modo simile al modo in cui viene archiviata una semplice proprietà stringa.

 

 
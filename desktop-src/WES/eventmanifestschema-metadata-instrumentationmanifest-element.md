---
title: Elemento metadata (instrumentationManifest)
description: Contiene valori globali a cui è possibile fare riferimento in altri manifesti.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- elemento metadata EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eaa22cc13c611b90ace42a2a71517fe0771d6e9ed03d6d964f11a4e4c93cda43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136324"
---
# <a name="metadata-instrumentationmanifest-element"></a>Elemento metadata (instrumentationManifest)

Contiene valori globali a cui è possibile fare riferimento in altri manifesti. Per un esempio, vedere il file Winmeta.xml incluso nella \\ cartella Include di Windows SDK.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

**L'elemento** metadata è definito dall'elemento [**instrumentationManifest.**](eventmanifestschema-instrumentationmanifest-element.md)

## <a name="remarks"></a>Commenti

Anche se è possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo userà. gli unici metadati che il servizio riconosce sono i metadati trovati nel file Winmeta.xml.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 






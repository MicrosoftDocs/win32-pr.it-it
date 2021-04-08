---
title: Elemento patternMap (PatternMapListType)
description: Definisce un mapping tra due espressioni regolari. Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- EventLog elemento patternMap
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047792"
---
# <a name="patternmap-patternmaplisttype-element"></a>Elemento patternMap (PatternMapListType)

Definisce un mapping tra due espressioni regolari. Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

L'elemento **patternMap** è definito dal tipo complesso [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 






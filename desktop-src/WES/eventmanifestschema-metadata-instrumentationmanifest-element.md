---
title: Elemento Metadata (instrumentationManifest)
description: Contiene i valori globali a cui è possibile fare riferimento in altri manifesti.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog elemento dei metadati
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119038"
---
# <a name="metadata-instrumentationmanifest-element"></a>Elemento Metadata (instrumentationManifest)

Contiene i valori globali a cui è possibile fare riferimento in altri manifesti. Per un esempio, vedere il file Winmeta.xml incluso nella \\ cartella di inclusione del Windows SDK.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

L'elemento **Metadata** viene definito dall'elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Commenti

Sebbene sia possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo utilizzerà. gli unici metadati riconosciuti dal servizio sono i metadati trovati nel file di Winmeta.xml.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 






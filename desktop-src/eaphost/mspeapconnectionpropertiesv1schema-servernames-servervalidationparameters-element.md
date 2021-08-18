---
title: Elemento ServerNames (ServerValidationParameters) (PEAP)
description: Informazioni sull'elemento ServerNames (ServerValidationParameters). Questo elemento rappresenta un elenco di nomi di server delimitati da punto e virgola. | Elemento ServerNames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- Elemento ServerNames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3f9de6ee28077b5206a9783ef7722864a479e1e5f26b78e4402ac79c6e4be5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984011"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Elemento ServerNames (ServerValidationParameters) (PEAP)

**L'elemento ServerNames (ServerValidationParameters)** rappresenta un elenco di nomi di server delimitati da punto e virgola.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

**L'elemento ServerNames** è definito dal [**tipo complesso ServerValidationParameters.**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)

## <a name="remarks"></a>Commenti

Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari. **L'elemento ServerNames** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Proprietà ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






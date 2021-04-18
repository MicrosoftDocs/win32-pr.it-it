---
title: Elemento ServerNames (ServerValidationParameters) (PEAP)
description: Informazioni sull'elemento ServerNames (ServerValidationParameters). Questo elemento rappresenta un elenco di nomi di server delimitati da punti e virgola. | Elemento ServerNames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- Nomeservers (elemento EAPHost)
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321278"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Elemento ServerNames (ServerValidationParameters) (PEAP)

L'elemento **serverNames (ServerValidationParameters)** rappresenta un elenco di nomi di server delimitati da punti e virgola.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

L'elemento **serverNames** viene definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Commenti

Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari. L'elemento **serverNames** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possibili elementi padre immediati nell'istanza dello schema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






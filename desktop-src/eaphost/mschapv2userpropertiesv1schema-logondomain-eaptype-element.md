---
title: Elemento LogonDomain (EapType)
description: Informazioni sull'elemento LogonDomain (EapType). Questo elemento identifica il dominio dell'utente o del computer da autenticare.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047348"
---
# <a name="logondomain-eaptype-element"></a>Elemento LogonDomain (EapType)

L'elemento **LogonDomain (EapType)** identifica il dominio dell'utente o del computer da autenticare.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

L'elemento **LogonDomain** è definito dall'elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se l'elemento **LogonDomain (EapType)** non è presente, viene usato il dominio da Winlogon. Questo elemento è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 






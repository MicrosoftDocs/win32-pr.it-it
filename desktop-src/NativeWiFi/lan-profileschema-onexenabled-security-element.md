---
description: Specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232427"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (Security)

L'elemento **OneXEnabled** (Security) specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 x. Quando **OneXEnabled** è false, il servizio di configurazione automatica non utilizza mai 802.1 x per l'autenticazione della porta. Quando **OneXEnabled** è true, il servizio di configurazione automatica tenta l'autenticazione della porta tramite 802.1 x.

Questo elemento è facoltativo. Il valore predefinito è TRUE. Quando **OneXEnabled** non viene specificato in un profilo, è possibile usare 802.1 x per l'autenticazione della porta.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

L'elemento **OneXEnabled** è definito dall'elemento [**Security**](lan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**sicurezza**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





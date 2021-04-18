---
description: Specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 X per l'autenticazione della porta.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314753"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (Security)

L'elemento **OneXEnforced** (Security) specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 x per l'autenticazione della porta. Quando **OneXEnforced** è true, il servizio di configurazione automatica deve usare 802.1 x per l'autenticazione della porta. Quando **OneXEnforced** è false, il servizio di configurazione automatica tenterà di utilizzare 802.1 x per l'autenticazione della porta, ma il servizio eseguirà il fallback a nessuna autenticazione se per qualsiasi motivo l'autenticazione 802.1 x non riesce.

Questo elemento è facoltativo. Il valore predefinito è FALSE.

Questo elemento ha un valore significativo solo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) è true. Se **OneXEnabled** è false, il valore di questo elemento viene ignorato.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

L'elemento **OneXEnforced** è definito dall'elemento [**Security**](lan-profileschema-security-msm-element.md) .

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

 

 





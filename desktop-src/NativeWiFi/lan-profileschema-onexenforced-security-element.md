---
description: Specifica se il servizio di configurazione automatica per le reti cablate richiede l'uso di 802.1X per l'autenticazione delle porte.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (security)
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
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798441"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (security)

**L'elemento OneXEnforced** (sicurezza) specifica se il servizio di configurazione automatica per le reti cablate richiede l'uso di 802.1X per l'autenticazione delle porte. Quando **OneXEnforced è** TRUE, il servizio di configurazione automatica deve usare 802.1X per l'autenticazione delle porte. Quando **OneXEnforced** è FALSE, il servizio di configurazione automatica tenterà di usare 802.1X per l'autenticazione tramite porta, ma il servizio non esegue il fall back a nessuna autenticazione se l'autenticazione 802.1X non riesce per qualsiasi motivo.

Questo elemento è facoltativo. Il valore predefinito è FALSE.

Questo elemento ha un valore significativo solo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) è TRUE. Se **OneXEnabled è** FALSE, il valore di questo elemento viene ignorato.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

**L'elemento OneXEnforced** è definito dall'elemento [**security.**](lan-profileschema-security-msm-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Sicurezza**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





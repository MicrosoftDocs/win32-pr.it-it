---
description: Specifica se il servizio di configurazione automatica per le reti cablate tenterà l'autenticazione delle porte usando 802.1X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (security)
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
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801091"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (security)

**L'elemento OneXEnabled** (sicurezza) specifica se il servizio di configurazione automatica per le reti cablate tenterà l'autenticazione tramite porta tramite 802.1X. Quando **OneXEnabled è** FALSE, il servizio di configurazione automatica non usa mai 802.1X per l'autenticazione delle porte. Quando **OneXEnabled è** TRUE, il servizio di configurazione automatica tenta l'autenticazione della porta usando 802.1X.

Questo elemento è facoltativo. Il valore predefinito è TRUE. Quando **OneXEnabled** non è specificato in un profilo, è possibile usare 802.1X per l'autenticazione delle porte.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

**L'elemento OneXEnabled** è definito dall'elemento [**di**](lan-profileschema-security-msm-element.md) sicurezza.

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

 

 





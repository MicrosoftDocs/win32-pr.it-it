---
title: Elemento EnableQuarantineChecks (EapType)
description: Informazioni sull'elemento EnableQuarantineChecks (EapType). Questo elemento indica se eseguire i controlli di protezione accesso alla rete (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963475"
---
# <a name="enablequarantinechecks-eaptype-element"></a>Elemento EnableQuarantineChecks (EapType)

L'elemento **EnableQuarantineChecks (EapType)** indica se eseguire i controlli di protezione accesso alla rete (NAP).

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

L'elemento **EnableQuarantineChecks** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se l'elemento **EnableQuarantineChecks** è true, PEAP eseguirà i controlli NAP; Se FALSE, PEAP non eseguirà controlli NAP. L'elemento **EnableQuarantineChecks** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






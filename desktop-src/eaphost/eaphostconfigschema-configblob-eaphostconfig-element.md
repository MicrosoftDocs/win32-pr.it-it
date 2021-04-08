---
title: Elemento ConfigBlob (EapHostConfig)
description: Viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato stringa di testo.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Elemento ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739695"
---
# <a name="configblob-eaphostconfig-element"></a>Elemento ConfigBlob (EapHostConfig)

L'elemento **ConfigBlob (EapHostConfig)** viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato stringa di testo.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

L'elemento **ConfigBlob** è definito dall'elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Commenti

Gli elementi [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e **ConfigBlob** non possono essere usati contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 






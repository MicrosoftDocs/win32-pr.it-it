---
title: Elemento Config (EapHostConfig)
description: Viene usato quando la configurazione del metodo è in formato testo XML anziché in un BLOB binario.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento Config EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba798afaa418e5de49c48abdc8dac242a300a7228ffe27a76241f4cbabed5833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739081"
---
# <a name="config-eaphostconfig-element"></a>Elemento Config (EapHostConfig)

**L'elemento Config (EapHostConfig)** viene usato quando la configurazione del metodo è in formato testo XML anziché in un BLOB binario.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

**L'elemento Config** è definito dall'elemento [**EapHostConfig.**](eaphostconfigschema-eaphostconfig-element.md)

## <a name="remarks"></a>Commenti

Gli **elementi Config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) non possono essere usati contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 






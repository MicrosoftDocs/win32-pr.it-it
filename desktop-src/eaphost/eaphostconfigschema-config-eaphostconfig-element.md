---
title: Elemento config (EapHostConfig)
description: Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento config EAPHost
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
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477170"
---
# <a name="config-eaphostconfig-element"></a>Elemento config (EapHostConfig)

L'elemento **config (EapHostConfig)** viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

L'elemento **config** è definito dall'elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Commenti

Gli elementi **config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) non possono essere usati contemporaneamente.

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

 

 






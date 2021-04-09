---
description: Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Elemento Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879406"
---
# <a name="compression-contexttype-element"></a>Elemento Compression (contextType)

L'elemento **Compression (ContextType)** specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.

Questo elemento può essere uno dei valori seguenti.

| Valore     | Significato                       |
|-----------|-------------------------------|
| Abilita  | Verrà utilizzata la compressione.     |
| DISABILITARE | Non verrà utilizzata la compressione. |



 

Questo elemento è facoltativo. Se questo elemento non è specificato, il sistema Mobile Broadband non utilizzerà la compressione.

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **Compression** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Contesto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 





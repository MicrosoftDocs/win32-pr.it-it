---
title: Tipo semplice GUIDType (schema di eventi)
description: Definisce un tipo di identificatore univoco globale nel formato del registro di sistema. | Tipo semplice GUIDType (schema di eventi)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Log eventi di tipo semplice GUIDType
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07635bc43ff07d65eee5f32786818ca7dad8dd64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352771"
---
# <a name="guidtype-simple-type-event-schema"></a>Tipo semplice GUIDType (schema di eventi)

Definisce un tipo di identificatore univoco globale nel formato del registro di sistema.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **GUIDType** è una stringa limitata dal modello seguente:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    Il valore deve essere un tipo di identificatore univoco globale nel formato del registro di sistema. Ad esempio, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Usare GUIDGen.exe o UUIDGen.exe per creare un GUID.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 






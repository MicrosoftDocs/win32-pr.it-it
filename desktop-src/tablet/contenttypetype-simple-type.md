---
description: Definisce il tipo che definisce i valori validi per l'attributo Type dell'elemento Content \[ Journal \] Reader.
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo semplice ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 83b49427e65bb5190554a0c995bec119de1230f0baab869ea4c5ce48dc5616f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008971"
---
# <a name="contenttypetype-simple-type"></a>Tipo semplice ContentTypeType

Definisce il tipo che definisce i valori validi per *l'attributo Type* dell'elemento Content [Journal \[ Reader. \]](content-element--journal-reader.md)

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice ContentTypeType** è una stringa limitata dal modello seguente:

-   `Normal|Inert`

## <a name="remarks"></a>Commenti

I valori validi sono "Normal" e "Inert".

Se il tipo è "Inert", il contenuto contenuto è una pagina Journal che rappresenta lo "sfondo" di sola lettura/non modificabile per il documento. Ciò si verifica quando viene creato un documento usando il driver della stampante Journal Note Writer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 





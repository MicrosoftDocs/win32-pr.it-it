---
title: Tipo complesso execType
description: Definisce gli elementi figlio e le informazioni di sequenziazione dell'elemento Exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Tipo complesso execType Utilità di pianificazione
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e0726930f902ec0458f42fff9cdce39026cf63ddab92982bc30da33ca671712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796631"
---
# <a name="exectype-complex-type"></a>Tipo complesso execType

Definisce gli elementi figlio e le informazioni di sequenziazione [**dell'elemento Exec (actionGroup).**](taskschedulerschema-exec-actiongroup-element.md)

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo                                                        | Descrizione                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Argomenti**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Specifica gli argomenti associati all'operazione della riga di comando. <br/>                              |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Specifica il file eseguibile o il documento da eseguire.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**Pathtype**](taskschedulerschema-pathtype-simpletype.md) | Specifica la directory in cui si trova il file eseguibile o i file utilizzati dal file eseguibile.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 






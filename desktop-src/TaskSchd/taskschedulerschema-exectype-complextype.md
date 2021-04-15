---
title: Tipo complesso execType
description: Definisce gli elementi figlio e le informazioni di sequenziazione dell'elemento Exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Utilità di pianificazione di tipo complesso execType
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475652"
---
# <a name="exectype-complex-type"></a>Tipo complesso execType

Definisce gli elementi figlio e le informazioni di sequenziazione dell'elemento [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .

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
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Specifica il file eseguibile o il documento da eseguire.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 






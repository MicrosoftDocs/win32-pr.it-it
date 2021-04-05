---
title: Esecuzione (SystemPropertiesType) (elemento)
description: Contiene informazioni sul processo e sul thread che hanno registrato l'evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- EventLog elemento esecuzione
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740359"
---
# <a name="execution-systempropertiestype-element"></a>Esecuzione (SystemPropertiesType) (elemento)

Contiene informazioni sul processo e sul thread che hanno registrato l'evento.

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L'elemento **Execution** viene definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome          | Tipo         | Descrizione                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| KernelTime    | unsignedInt  | Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in unità di tempo della CPU.<br/>                        |
| ProcessID     | unsignedInt  | Identifica il processo che ha generato l'evento.<br/>                                               |
| ProcessorID   | unsignedByte | Numero di identificazione del processore che ha elaborato l'evento.<br/>                          |
| ProcessorTime | unsignedInt  | Per le sessioni private ETW, il tempo di esecuzione trascorso per le istruzioni in modalità utente, in cicli della CPU.<br/> |
| SessionID     | unsignedInt  | Numero di identificazione per la sessione di Terminal Server in cui si è verificato l'evento.<br/>         |
| ThreadID      | unsignedInt  | Identifica il thread che ha generato l'evento.<br/>                                                |
| Tempi      | unsignedInt  | Tempo di esecuzione trascorso per le istruzioni in modalità utente, in unità di tempo della CPU.<br/>                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 






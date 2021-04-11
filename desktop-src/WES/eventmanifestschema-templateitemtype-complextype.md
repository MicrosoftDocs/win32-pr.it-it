---
title: Tipo complesso TemplateItemType
description: Modello che definisce i dati da includere in un evento. | Tipo complesso TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Log eventi di tipo complesso TemplateItemType
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234774"
---
# <a name="templateitemtype-complex-type"></a>Tipo complesso TemplateItemType

Modello che definisce i dati da includere in un evento.

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Tipo                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**binario**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | Riservato esclusivamente per uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**dati**](eventmanifestschema-data-templateitemtype-element.md)         | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)     | Definisce un elemento di dati che si desidera includere nell'evento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**struct**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento. I provider scrivono la struttura come un BLOB e non come singoli membri della struttura.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | Frammento XML utilizzato per eseguire il rendering dei dati dell'evento. Se non si include il frammento, i dati dell'evento vengono visualizzati nell'ordine in cui gli elementi di dati sono definiti nel modello. Il contenuto di questo elemento è qualsiasi frammento XML valido. Il frammento deve contenere solo un nodo di primo livello e il nodo di primo livello deve specificare il proprio spazio dei nomi. <br/> Per fare riferimento a un elemento dati nel frammento, impostare il corpo del testo per un nodo nel frammento su%*n*, dove *n* è l'indice in base uno degli elementi di dati di primo livello nell'elenco di elementi di dati (non è possibile fare riferimento ai membri di una struttura). Il valore di indice specificato non deve essere maggiore del numero di elementi di dati di primo livello nel modello.<br/> Questo elemento segue tutti i **dati** e gli elementi **struct** . <br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name | string | Riservato esclusivamente per uso interno.<br/>                                                                                                                                                            |
| name | string | Nome del modello.<br/>                                                                                                                                                                  |
| tid  | token  | Identificatore che identifica in modo univoco il modello all'interno dell'elenco di modelli definiti dal provider. Utilizzare questo nome per fare riferimento al modello quando si definisce la definizione dell'evento.<br/> |



## <a name="remarks"></a>Commenti

La definizione del modello deve contenere almeno un elemento figlio data o struct. Il provider deve scrivere i dati dell'evento nell'ordine degli elementi di dati definiti nel modello.

La dimensione di tutti gli elementi di dati nel modello deve essere inferiore a 64 KB.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come creare una definizione di modello.


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 






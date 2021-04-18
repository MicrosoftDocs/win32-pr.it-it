---
title: Tipo complesso TaskType
description: Definisce un componente o un sottocomponente di un'applicazione. | Tipo complesso TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Log eventi di tipo complesso TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321874"
---
# <a name="tasktype-complex-type"></a>Tipo complesso TaskType

Definisce un componente o un sottocomponente di un'applicazione.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Tipo                                                                     | Descrizione                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**OpCodes**](eventmanifestschema-opcodes-tasktype-element.md) | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) | Definisce un elenco di codici operativi specifici dell'attività. Non è possibile usare i valori opcode definiti in Winmeta.xml per i codici operativi specifici dell'attività.<br/> |



## <a name="attributes"></a>Attributi



| Nome      | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventGUID | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identificatore univoco globale, nel formato del registro di sistema, che identifica l'attività. Questo attributo è obbligatorio se si usa l'argomento del compilatore del messaggio-MOF per generare una classe MOF per il supporto di livello inferiore.<br/>                                                                                                   |
| message   | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per l'attività. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                   |
| name      | **QName**                                                         | Nome dell'attività.<br/>                                                                                                                                                                                                                                                                                 |
| simbolo    | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento all'attività nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per l'attività nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Valore numerico che identifica in modo univoco questa attività nell'elenco delle attività definite dal provider. Il valore deve essere compreso tra 1 e 239.<br/>                                                                                                                                             |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come specificare un'attività.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 






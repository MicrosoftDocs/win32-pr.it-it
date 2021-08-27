---
title: Tipo complesso KeywordType
description: Definisce una parola chiave che identifica una categoria di eventi. | Tipo complesso KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- EventLog di tipo complesso KeywordType
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d444c39796f741cd800fb393527e5adca6e50cef05de0c55c1def2bb40142a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124381"
---
# <a name="keywordtype-complex-type"></a>Tipo complesso KeywordType

Definisce una parola chiave che identifica una categoria di eventi. Una parola chiave è un tag che viene associato a un evento per raggruppare gli eventi in base al relativo utilizzo.

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mask    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Maschera di bit che deve avere un solo bit impostato. Il bit rappresenta una categoria di eventi, ad esempio eventi di lettura o di scrittura. È possibile specificare valori di bit nell'intervallo da 0x0000000000000001 a 0x0000800000000000 (bit da 0 a 47).<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per la parola chiave. La stringa del messaggio fa riferimento a una stringa localizzata [**nella sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto.<br/>                                                                                                       |
| name    | **QName**                                                         | Nome della parola chiave. Il nome deve essere univoco all'interno dell'elenco di parole chiave definite dal provider.<br/>                                                                                                                                                                                                     |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da usare per fare riferimento alla parola chiave nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la parola chiave nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="remarks"></a>Commenti

Il Winmeta.xml file incluso in Windows SDK contiene un elenco di parole chiave. Queste parole chiave sono riservate e non devono essere usate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 






---
title: Tipo complesso EventsType
description: Contiene un elenco di provider definiti nel manifesto. | Tipo complesso EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventLog di tipo complesso EventsType
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d0cee50c0332d283c439448fd80c7abe319fec5065f39dcad4e053baf600bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055989"
---
# <a name="eventstype-complex-type"></a>Tipo complesso EventsType

Contiene un elenco di provider definiti nel manifesto.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio

| Elemento | Tipo | Descrizione |
|---------|------|-------------|
| message |      | Definisce una stringa di messaggio. |
| messageTable | | Definisce un elenco di stringhe di messaggio. Non è necessario usare una tabella dei messaggi tranne nei casi seguenti in cui è necessario definire una tabella dei messaggi per assegnare in modo esplicito i numeri di risorsa alle stringhe di messaggio. <ul><li>Si esegue la migrazione da un file di testo di messaggio (con estensione mc) a un manifesto, ma si scrivono comunque eventi nei canali di applicazione e di sistema, in modo che i consumer legacy continuino a utilizzare gli eventi. Per eseguire questa operazione, gli identificatori di risorsa per le stringhe di messaggio definite nel manifesto devono essere gli stessi degli identificatori di evento. Tuttavia, il compilatore di messaggi assegna automaticamente gli identificatori di risorsa alle stringhe di messaggio. Per eseguire l'override del compilatore, usare la tabella dei messaggi e impostare l'attributo value sull'identificatore evento e l'attributo del messaggio in modo che faccia riferimento a una stringa nella tabella di stringhe nella sezione localizzazione del manifesto.</li><li>Se si vogliono identificare più di 16 provider, è necessario includere la tabella dei messaggi che il diciassettesmo e nei provider devono usare per assegnare valori di risorsa per le stringhe di messaggio definite. Se il provider fa riferimento a stringhe di messaggio definite dai provider da 1 a 16, tali stringhe non vengono incluse nella tabella dei messaggi.</li></ul>|
| [**Provider**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Elenco di provider che si desidera definire. |

## <a name="attributes"></a>Attributi

| Nome    | Tipo                                                             | Descrizione                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Riferimento alla stringa localizzata nella tabella delle stringhe.                               |
| mid     | xs:string                                                        | Non usato.                                                                              |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nome simbolico che si desidera che il compilatore di messaggi crei per questa stringa di messaggio.|
| Valore   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Numero da utilizzare come identificatore del messaggio.                          |


## <a name="remarks"></a>Commenti

Il limite pratico del numero di provider che è possibile definire in un manifesto è 16 provider. Se si specificano più di 16 provider, è necessario usare una tabella di messaggi per assegnare in modo esplicito i numeri di risorsa alle stringhe di messaggio a cui fa riferimento il provider. Per altri dettagli, vedere l'elemento message precedente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop di Vista\]       |
| Server minimo supportato | Windows Solo app desktop server 2008 \[\] |

---
title: Tipo complesso EventsType
description: Contiene un elenco di provider definiti nel manifesto. | Tipo complesso EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Log eventi di tipo complesso EventsType
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321539"
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
| messageTable | | Definisce un elenco di stringhe di messaggio. Non è necessario utilizzare una tabella messaggi tranne nei casi seguenti, in cui è necessario definire una tabella messaggi per assegnare in modo esplicito i numeri delle risorse alle stringhe di messaggio. <ul><li>Si esegue la migrazione da un file di testo del messaggio (. MC) a un manifesto, ma si stanno ancora scrivendo eventi ai canali dell'applicazione e di sistema, in modo che i consumer legacy continuino a utilizzarli. Per eseguire questa operazione, gli identificatori di risorsa per le stringhe di messaggio definite nel manifesto devono corrispondere agli identificatori di evento. Tuttavia, il compilatore di messaggi assegna automaticamente gli identificatori di risorsa alle stringhe di messaggio. Per eseguire l'override del compilatore, utilizzare la tabella Message e impostare l'attributo value sull'identificatore dell'evento e l'attributo Message per fare riferimento a una stringa nella tabella di stringhe nella sezione localizzazione del manifesto.</li><li>Se si desidera identificare più di 16 provider, è necessario includere la tabella dei messaggi che i provider XVII e su devono utilizzare per assegnare i valori delle risorse per le stringhe di messaggio definite. Se il provider fa riferimento a stringhe di messaggio che sono definite da 1 a 16, le stringhe di messaggio non vengono incluse nella tabella messaggi.</li></ul>|
| [**provider**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Elenco di provider che si desidera definire. |

## <a name="attributes"></a>Attributi

| Nome    | Tipo                                                             | Descrizione                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Riferimento alla stringa localizzata nella tabella di stringhe.                               |
| mid     | xs:string                                                        | Non usato.                                                                              |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.|
| Valore   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Numero da utilizzare come identificatore del messaggio per questo messaggio.                          |


## <a name="remarks"></a>Commenti

Il limite pratico del numero di provider che è possibile definire in un manifesto è 16 provider. Se si specificano più di 16 provider, è necessario utilizzare una tabella messaggi per assegnare in modo esplicito i numeri delle risorse alle stringhe di messaggio a cui fa riferimento il provider. Per ulteriori informazioni, vedere l'elemento Message sopra riportato.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows Vista\]       |
| Server minimo supportato | \[Solo app desktop Windows Server 2008\] |

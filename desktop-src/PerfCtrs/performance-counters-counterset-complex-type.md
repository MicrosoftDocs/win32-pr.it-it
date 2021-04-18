---
description: Definisce un elenco di contatori correlati logicamente.
ms.assetid: d094146a-389e-4053-8ee5-acd29254e817
title: Tipo complesso del contatore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e753fab4308f1e981ab06e9470742ace46840a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312131"
---
# <a name="counterset-complex-type"></a>Tipo complesso del contatore

Definisce un elenco di contatori correlati logicamente.

``` syntax
<xs:complexType name="counterSet">
    <xs:sequence>
        <xs:element name="structs"
            type="man:structs"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="counter"
            type="man:counter"
            minOccurs="1"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="required"
     />
    <xs:attribute name="guid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="instances"
        use="optional"
        default="single"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="single"
                 />
                <xs:enumeration
                    value="multiple"
                 />
                <xs:enumeration
                    value="globalAggregate"
                 />
                <xs:enumeration
                    value="multipleAggregate"
                 />
                <xs:enumeration
                    value="globalAggregateHistory"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento     | Tipo                                                             | Descrizione                                                                                            |
|-------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| **Counter** | [**uomo: contatore**](performance-counters-counter-complex-type.md) | Definisce un contatore fornito dal provider.<br/>                                               |
| **strutture** | [**struct uomo:**](performance-counters-structs-complex-type.md) | Elenco di elementi struct che contengono valori per i contatori definiti in questo insieme di contatori.<br/> |



## <a name="attributes"></a>Attributi



| Nome        | Tipo                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| description | **xs:string**                                                           | Breve descrizione dell'insieme di contatori. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| guid        | [**uomo: GUIDType**](performance-counters-guidtype-simple-type.md)       | GUID che identifica in modo univoco l'insieme di contatori. La registrazione dell'insieme di contatori non riesce se il GUID è già registrato. Per aggiornare un insieme di contatori registrato, è necessario prima disinstallare l'insieme di contatori e quindi registrarlo di nuovo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| instances   |                                                                         | Determina se l'insieme di contatori può contenere più istanze. Di seguito sono elencati i valori possibili:<br/> <dl> <dt><span id="single"></span><span id="SINGLE"></span>singolo</dt> <dd> Definisce un insieme di contatori in cui possono esistere solo un'istanza dei contatori nell'insieme di contatori. Specificare questo valore se i contatori forniscono misure a livello di sistema, ad esempio la memoria fisica. Questo è il valore predefinito.<br/> </dd> <dt><span id="multiple"></span><span id="MULTIPLE"></span>più</dt> <dd> Definisce un insieme di contatori in cui possono esistere più istanze dei contatori nell'insieme di contatori. Specificare questo valore se i contatori forniscono misure per istanza, ad esempio il tempo processore per processo.<br/> </dd> <dt><span id="globalAggregate"></span><span id="globalaggregate"></span><span id="GLOBALAGGREGATE"></span>globalAggregate</dt> <dd> Definisce un set di contatori a istanza singola in cui i contatori nell'insieme di contatori devono essere aggregati da diverse origini attive. Ad esempio, è possibile creare un insieme di contatori contenente un contatore che conta il numero di letture del disco per un disco rigido. Se il computer dispone di tre dischi rigidi e di un consumer di query per il numero di letture del disco, PERFLIB otterrà il numero di letture da ogni disco e sommerà i singoli valori. <br/> </dd> <dt><span id="multipleAggregate"></span><span id="multipleaggregate"></span><span id="MULTIPLEAGGREGATE"></span>multipleAggregate</dt> <dd> Definisce un insieme di contatori a più istanze in cui i contatori nell'insieme di contatori devono essere aggregati in tutte le istanze di tale contatore. Ad esempio, è possibile creare un insieme di contatori per un'applicazione multithread contenente un contatore che misura le prestazioni del thread (ogni thread fa riferimento a un'istanza dell'insieme di contatori). Quando un consumer esegue una query sul contatore del tempo totale di esecuzione del thread, PERFLIB somma il tempo totale di esecuzione del thread di ogni istanza.<br/> </dd> <dt><span id="globalAggregateHistory"></span><span id="globalaggregatehistory"></span><span id="GLOBALAGGREGATEHISTORY"></span>globalAggregateHistory</dt> <dd> Definisce un insieme di contatori a istanza singola i cui valori dei contatori vengono memorizzati nella cache per la durata del consumer. Si noti che tutti i contatori nell'insieme di contatori vengono memorizzati nella cache. Per memorizzare nella cache solo contatori specifici, decorare questi contatori con l'attributo History.<br/> Utilizzando l'esempio di lettura del disco da globalAggregate, tutti i valori dei contatori nell'insieme di contatori verrebbero memorizzati nella cache. Se un disco non è più disponibile, l'ultimo valore memorizzato nella cache per i byte totali letti dal disco sarebbe ancora disponibile per l'applicazione consumer.<br/> </dd> </dl> |
| name        |                                                                         | Nome visualizzato dell'insieme di contatori. Deve essere minore di 1.024 caratteri. Per il nome è prevista la distinzione tra maiuscole e minuscole. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| simbolo      | [**uomo: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nome simbolico che identifica l'insieme di contatori. Lo strumento [CTRPP](ctrpp.md) crea una variabile GUID che è possibile usare quando si chiamano le funzioni che richiedono il GUID dell'insieme di contatori (ad esempio, [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)). Il nome della variabile è nel formato, *simbolico* GUID. <br/> Se si include l'argomento **-Prefix** quando si chiama [CTRPP](ctrpp.md), la stringa di prefisso viene aggiunta all'inizio del nome simbolico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Uri         | **XS: anyURI**                                                           | Identificatore univoco della risorsa uniforme che consente agli utenti di accedere ai contatori nell'insieme di contatori da qualsiasi posizione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





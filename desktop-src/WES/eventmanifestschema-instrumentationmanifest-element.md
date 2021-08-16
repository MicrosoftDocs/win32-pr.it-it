---
title: Elemento instrumentationManifest
description: Nodo radice del manifesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- Elemento instrumentationManifest EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343722"
---
# <a name="instrumentationmanifest-element"></a>Elemento instrumentationManifest

Nodo radice del manifesto.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                        | Tipo                                                                               | Descrizione                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Strumentazione**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**Tipo di strumentazione**](eventmanifestschema-instrumentationtype-complextype.md) | Questa sezione definisce uno o più provider di eventi e gli eventi che registrano.<br/>                                                                                                                                                                                                                     |
| [**Localizzazione**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)       | In questa sezione vengono definite le stringhe di messaggio localizzate usate dai consumer per la visualizzazione. Ad esempio, questa sezione conterrà la stringa di messaggio localizzata per il nome del provider, gli eventi definiti dall'utente e gli eventuali attributi di evento definiti, ad esempio canali, attività e codici operativo.<br/> |
| [**Metadati**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**Tipo di metadati**](eventmanifestschema-metadatatype-complextype.md)               | Questa sezione definisce i tipi di metadati che possono essere utilizzati da altri manifesti. Per un esempio, vedere il file Winmeta.xml incluso nella \\ cartella Include di Windows SDK.<br/>                                                                                                                                    |



## <a name="remarks"></a>Commenti

**L'elemento instrumentationManifest** deve contenere gli spazi dei nomi seguenti:

<dl> xmlns=" https://schemas.microsoft.com/win/2004/08/events "  
xmlns:win=" https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns:xs=" https://www.w3.org/2001/XMLSchema "  
</dl>

Un manifesto deve contenere una sezione di strumentazione e una sezione di localizzazione. La sezione di strumentazione e la sezione dei metadati si escludono a vicenda (non è possibile definire entrambi nello stesso manifesto). Anche se è possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo userà. gli unici metadati che il servizio riconosce sono i metadati trovati nel file Winmeta.xml.

## <a name="examples"></a>Esempio

L'esempio seguente illustra lo scheletro di un manifesto di strumentazione completamente definito.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 






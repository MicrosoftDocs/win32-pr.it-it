---
title: Tipo complesso LevelType
description: Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Tipo complesso LevelType EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b80e034f6b77f869207ecb785edbb935841eed2dba6bde73ad88c441dabf15cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055939"
---
# <a name="leveltype-complex-type"></a>Tipo complesso LevelType

Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.

``` syntax
<xs:complexType name="LevelType"
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
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il livello. La stringa del messaggio fa riferimento a una stringa localizzata nella [**sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                    |
| name    | **QName**                                                         | Nome da assegnare a questo livello. Questo nome deve essere univoco nell'ambito del provider.<br/>                                                                                                                                                                                                            |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al livello nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il livello nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore del livello. È possibile specificare valori nell'intervallo da 16 a 255. Per i valori di livello predefiniti, vedere Note.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori di livello predefiniti che è possibile usare. Questi valori sono definiti nel file Winmeta.xml incluso nell'SDK Windows.



| Nome              | Valore | Simbolo                    | Descrizione                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | WINEVENT \_ LEVEL \_ CRITICAL | Identifica un evento di uscita o terminazione anomalo.<br/>            |
| win:Error         | 2     | ERRORE A \_ LIVELLO DI \_ WINEVENT    | Identifica un evento di errore grave.<br/>                             |
| win:Warning       | 3     | AVVISO A \_ LIVELLO DI \_ WINEVENT  | Identifica un evento di avviso, ad esempio un errore di allocazione.<br/>    |
| win:Informational | 4     | INFORMAZIONI SUL \_ LIVELLO \_ WINEVENT     | Identifica un evento non di errore, ad esempio un evento di ingresso o di uscita.<br/> |
| win:Verbose       | 5     | LIVELLO \_ DI WINEVENT \_ DETTAGLIATO  | Identifica un evento di traccia dettagliato.<br/>                           |



 

I numeri più elevati implicano che si ottengono anche livelli inferiori. Ad esempio, se si specifica win:Warning, vengono visualizzati tutti gli eventi di avviso, errore ed eventi critici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 






---
title: Tipo complesso LevelType
description: Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Log eventi di tipo complesso LevelType
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119039"
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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il livello. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                    |
| name    | **QName**                                                         | Nome da assegnare a questo livello. Questo nome deve essere univoco all'interno dell'ambito del provider.<br/>                                                                                                                                                                                                            |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da usare per fare riferimento al livello nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il livello nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore del livello. È possibile specificare valori compresi tra 16 e 255. Per i valori di livello predefiniti, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori di livello predefiniti che è possibile utilizzare. Questi valori vengono definiti nel file di Winmeta.xml incluso nel Windows SDK.



| Nome              | Valore | Simbolo                    | Descrizione                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | livello di WINEVENT \_ \_ critico | Identifica un evento di chiusura o chiusura anomalo.<br/>            |
| win:Error         | 2     | \_errore a livello di WINEVENT \_    | Identifica un evento di errore grave.<br/>                             |
| win:Warning       | 3     | \_avviso livello \_ WINEVENT  | Identifica un evento di avviso, ad esempio un errore di allocazione.<br/>    |
| win:Informational | 4     | \_informazioni sul livello di WINEVENT \_     | Identifica un evento non di errore, ad esempio un evento di ingresso o di uscita.<br/> |
| win:Verbose       | 5     | \_dettagliato livello \_ WINEVENT  | Identifica un evento di traccia dettagliato.<br/>                           |



 

I numeri più alti implicano che si ottengono anche livelli inferiori. Se ad esempio si specifica Win: Warning, vengono visualizzati tutti gli eventi di avviso, di errore e di importanza critica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 






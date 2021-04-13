---
description: L' <simpleLocation> elemento specifica il percorso per i connettori di ricerca che sono basati sul file System o sul gestore del protocollo. Questo elemento ha due elementi figlio e nessun attributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342901"
---
# <a name="simplelocation-element-search-connector-schema"></a>Elemento simpleLocation (schema del connettore di ricerca)

L' <simpleLocation> elemento specifica il percorso per i connettori di ricerca che sono basati sul file System o sul gestore del protocollo. Questo elemento ha due elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento URL simpleLocation (schema del connettore di ricerca)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialized: questo elemento contiene il ShellLink con codifica Base64 che punta alla posizione definita nell' <url> elemento. Windows 7 crea il ShellLink dal valore dell' <url> elemento e aggiorna correttamente questo campo al primo caricamento della libreria, quindi deve essere lasciato vuoto dall'autore. |



 

## <a name="remarks"></a>Commenti

Questo elemento può essere utilizzato anziché <locationProvider> quando il percorso si trova nel file System o il connettore è un gestore di protocollo noto, ad esempio MAPI:). Se <simpleLocation> è presente, non deve essere un <locationProvider> elemento. Per i connettori di ricerca del provider di servizi Web, usare [<locationProvider>](search-schema-sconn-locationprovider.md) invece l'elemento.

## <a name="examples"></a>Esempi


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 




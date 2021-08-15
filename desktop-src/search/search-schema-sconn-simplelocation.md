---
description: L'elemento specifica il percorso per i connettori di ricerca basati sul <simpleLocation> file system o sul gestore di protocollo. Questo elemento ha due elementi figlio e nessun attributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82731c5a230f8dd12b9d73cafd75dfc7d3cdd66bf1e57120701ed3ca0ba54b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862462"
---
# <a name="simplelocation-element-search-connector-schema"></a>Elemento simpleLocation (schema del connettore di ricerca)

L'elemento specifica il percorso per i connettori di ricerca basati sul <simpleLocation> file system o sul gestore di protocollo. Questo elemento ha due elementi figlio e nessun attributo.

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
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento simpleLocation url (schema del connettore di ricerca)](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | serialized: questo elemento contiene l'elemento ShellLink con codifica Base64 che punta alla posizione definita <url> nell'elemento . Windows 7 crea ShellLink dal valore dell'elemento e aggiorna correttamente questo campo al primo caricamento di questa libreria, in modo che venga lasciato vuoto <url> dall'autore. |



 

## <a name="remarks"></a>Commenti

Questo elemento può essere usato invece di quando la posizione si trova nel file system o il connettore è un gestore di protocollo noto <locationProvider> (ad esempio mapi:). Se <simpleLocation> è presente, NON DEVE essere presente un <locationProvider> elemento . Per i connettori di ricerca del provider di servizi Web, usare [<locationProvider>](search-schema-sconn-locationprovider.md) invece l'elemento .

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



 

 




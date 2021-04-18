---
description: L' <imageLink> elemento facoltativo specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento Collegamentoimmagine (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306086"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento Collegamentoimmagine (schema del connettore di ricerca)

L' <imageLink> elemento facoltativo specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento URL Collegamentoimmagine (schema del connettore di ricerca)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Commenti

Il valore Collegamentoimmagine può essere un percorso di file system locale o un URL. Il file di immagine può essere qualsiasi tipo di immagine di base supportato da Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Esempio di elemento Collegamentoimmagine


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




---
description: L' <url> elemento specifica un URL per l'anteprima per questo connettore di ricerca. Se <imageLink> esiste, questo elemento è obbligatorio. Non ha elementi figlio e nessun attributo.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Elemento URL Collegamentoimmagine (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306087"
---
# <a name="imagelink-url-element-search-connector-schema"></a>Elemento URL Collegamentoimmagine (schema del connettore di ricerca)

L' <url> elemento specifica un URL per l'anteprima per questo connettore di ricerca. Se <imageLink> esiste, questo elemento è obbligatorio. Non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- url -->
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



| Elemento padre                                                                   | Elementi figlio |
|----------------------------------------------------------------------------------|----------------|
| [Elemento Collegamentoimmagine (schema del connettore di ricerca)](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a>Commenti

Il valore può essere un percorso di file system locale o un URL. Il file di immagine può essere qualsiasi tipo di immagine di base supportato da Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelinkurl-element"></a>Esempio di elemento imageLinkurl


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




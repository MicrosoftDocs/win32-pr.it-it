---
description: L'elemento <imageLink> facoltativo specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ad8c2500e2739210646c446d9f906d5a83571ea4ac9780ab9136b73805c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711091"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (schema del connettore di ricerca)

L'elemento <imageLink> facoltativo specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.

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
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento imageLink url (schema del connettore di ricerca)](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a>Commenti

Il valore imageLink può essere un percorso di file system locale o un URL. Il file di immagine può essere uno dei tipi di immagine di base supportati da Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Esempio di elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




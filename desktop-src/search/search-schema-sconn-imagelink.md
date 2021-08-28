---
description: "&lt;L'elemento facoltativo imageLink &gt; specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo."
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento imageLink (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6030f44e74f8f8441b3a6cd0835df9c5969619
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882390"
---
# <a name="imagelink-element-search-connector-schema"></a>Elemento imageLink (schema del connettore di ricerca)

&lt;L'elemento facoltativo imageLink &gt; specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.

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

Il valore imageLink può essere un percorso file system o un URL. Il file di immagine può essere uno dei tipi di immagine di base supportati da Windows 7 (PNG, BMP, JPG, GIF).

## <a name="example-of-an-imagelink-element"></a>Esempio di elemento imageLink


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 




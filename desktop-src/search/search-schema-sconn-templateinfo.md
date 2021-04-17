---
description: Questo <templateInfo> elemento facoltativo specifica un tipo di cartella per visualizzare i risultati di una query su questo connettore di ricerca. Questo elemento non ha attributi e un solo figlio obbligatorio.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306074"
---
# <a name="templateinfo-element-search-connector-schema"></a>Elemento templateInfo (schema del connettore di ricerca)

Questo <templateInfo> elemento facoltativo specifica un tipo di cartella per visualizzare i risultati di una query su questo connettore di ricerca. Questo elemento non ha attributi e un solo figlio obbligatorio.

## <a name="syntax"></a>Sintassi


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento folderType (schema del connettore di ricerca)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Commenti

Se non si specifica un tipo di cartella particolare nell' <templateInfo> elemento, Windows usa il tipo di cartella del connettore di ricerca generale {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Esempio di elemento templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 




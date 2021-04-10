---
description: L' <depth> elemento specifica se l'ambito del connettore di ricerca deve includere URL figlio. I valori consentiti sono Deep e Shallow. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Elemento Depth (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966532"
---
# <a name="depth-element-search-connector-schema"></a>Elemento Depth (Schema connettore di ricerca)

L' <depth> elemento specifica se l'ambito del connettore di ricerca deve includere URL figlio. I valori consentiti sono `Deep` e `Shallow`. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- depth -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
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
| [Elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Commenti

Se la profondità è profonda, gli utenti possono sfogliare o cercare gli elementi nel livello URL di scopeItem o in qualsiasi URL figlio.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ FolderA e tutte le relative cartelle figlio e c: \\ FolderB ma nessuna delle relative cartelle figlio.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




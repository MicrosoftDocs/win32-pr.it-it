---
description: L' <folderType> elemento specifica il GUID per il tipo di cartella. Questo elemento è obbligatorio se l' <templateInfo> elemento esiste. Non ha attributi e nessun elemento figlio.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento folderType (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484404"
---
# <a name="foldertype-element-search-connector-schema"></a>Elemento folderType (schema del connettore di ricerca)

L' <folderType> elemento specifica il GUID per il tipo di cartella. Questo elemento è obbligatorio se l' <templateInfo> elemento esiste. Non ha attributi e nessun elemento figlio.

## <a name="syntax"></a>Sintassi


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                         | Elementi figlio |
|----------------------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (schema del connettore di ricerca)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Commenti

Il GUID predefinito è {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un tipo di cartella generale per i connettori di ricerca federata (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Esempio di elemento folderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 




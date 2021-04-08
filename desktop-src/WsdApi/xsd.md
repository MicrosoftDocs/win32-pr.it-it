---
description: Specifica un file XSD da elaborare per le informazioni sul contratto.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: XSD (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103881981"
---
# <a name="xsd-element"></a>XSD (elemento)

Specifica un file XSD da elaborare per le informazioni sul contratto.

## <a name="usage"></a>Utilizzo

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Attributi



| Attributo           | Type                       | Obbligatoria       | Descrizione                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | stringa PathName<br/> | Sì<br/> | File e percorso del file di input XSD.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                               | Descrizione                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Specifica un tipo da includere da un file XSD.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

La stringa del nome file deve includere anche informazioni complete sul percorso.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 





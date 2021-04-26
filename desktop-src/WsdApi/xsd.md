---
description: Specifica un file XSD da elaborare per le informazioni sul contratto.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: Elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994548"
---
# <a name="xsd-element"></a>Elemento xsd

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
| **path**<br/> | stringa pathname<br/> | Sì<br/> | File e percorso del file di input XSD.<br/> <br/> |



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



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 





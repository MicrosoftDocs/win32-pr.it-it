---
description: Genera implementazioni per le funzioni QueryInterface, AddRef e release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310295"
---
# <a name="iunknowndefinitions-element"></a>Elemento IUnknownDefinitions

Genera implementazioni per le funzioni QueryInterface, AddRef e release.

## <a name="usage"></a>Utilizzo

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Attributi



| Attributo                  | Type                         | Obbligatoria       | Descrizione                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | stringa di caratteri \_<br/> | Sì<br/> | Nome della classe di implementazione.<br/> <br/> |
| **refCountVar**<br/> | stringa di caratteri \_<br/> | Sì<br/> | Nome della variabile di conteggio dei riferimenti.<br/> <br/>  |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**interfaccia**](interface.md)<br/> | Nome dell'interfaccia che deve essere restituita da QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
interface
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 





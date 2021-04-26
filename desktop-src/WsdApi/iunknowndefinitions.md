---
description: Genera implementazioni per le funzioni QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995148"
---
# <a name="iunknowndefinitions-element"></a>Elemento IUnknownDefinitions

Genera implementazioni per le funzioni QueryInterface, AddRef e Release.

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
| **classe proxy**<br/>  | stringa di \_ caratteri<br/> | Sì<br/> | Nome della classe di implementazione.<br/> <br/> |
| **refCountVar**<br/> | stringa di \_ caratteri<br/> | Sì<br/> | Nome della variabile del conteggio dei riferimenti.<br/> <br/>  |



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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 





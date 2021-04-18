---
description: Specifica il provider di detouring Microsoft Media Foundation, che traccia Media Foundation chiamate API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308409"
---
# <a name="mfdetours-element"></a>elemento mfdetours

Specifica il provider di detouring Microsoft Media Foundation, che traccia Media Foundation chiamate API.

## <a name="usage"></a>Utilizzo

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Attributi



| Attributo            | Type             | Obbligatoria       | Descrizione                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Sì<br/> | Livello di traccia.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                               |
|---------------------------------------|
| [**parola chiave**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                   |
|-------------------------------------------|
| [**provider**](providers.md)<br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|              |     |
|--------------|-----|
| Può essere vuoto | No  |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 





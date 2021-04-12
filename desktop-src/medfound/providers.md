---
description: Contiene un elenco di provider di traccia per MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Providers (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226510"
---
# <a name="providers-element"></a>Providers (elemento)

Contiene un elenco di provider di traccia per [MFTrace](mftrace.md).

## <a name="usage"></a>Utilizzo

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | Specifica il provider di detouring Media Foundation, che traccia Media Foundation chiamate API.<br/> <br/> |
| [**provider**](provider.md)<br/>   | Specifica un provider di traccia (ETW o WPP).<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Elementi padre

Non ci sono elementi padre.

## <a name="element-information"></a>Informazioni sull'elemento



|              |     |
|--------------|-----|
| Può essere vuoto | Sì |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 





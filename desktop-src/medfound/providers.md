---
description: Contiene un elenco di provider di traccia per MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118486"
---
# <a name="providers-element"></a>Elemento providers

Contiene un elenco di provider di traccia per [MFTrace.](mftrace.md)

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
| [**mfdetours**](mfdetours.md)<br/> | Specifica il provider Media Foundation Detours, che traccia Media Foundation chiamate API.<br/> <br/> |
| [**Provider**](provider.md)<br/>   | Specifica un provider di traccia (ETW o WPP).<br/> <br/>                                                  |



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

:::row:::
    :::column:::
        Può essere vuoto
    :::column-end:::
    :::column span="2":::
        Sì
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione di MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 





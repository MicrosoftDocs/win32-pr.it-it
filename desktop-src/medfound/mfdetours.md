---
description: Specifica il provider Microsoft Media Foundation Detours, che traccia Media Foundation chiamate API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: Elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119336"
---
# <a name="mfdetours-element"></a>Elemento mfdetours

Specifica il provider Microsoft Media Foundation Detours, che traccia Media Foundation chiamate API.

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
| [**Parola chiave**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementi padre

| Elemento                                   |
|-------------------------------------------|
| [**Provider**](providers.md)<br/> |



## <a name="element-information"></a>Informazioni sull'elemento

:::row:::
    :::column:::
        Può essere vuoto
    :::column-end:::
    :::column span="2":::
        No
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione di MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 





---
description: Specifica il provider Microsoft Media Foundation Detours, che traccia Media Foundation chiamate API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: Elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113641"
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

 

 





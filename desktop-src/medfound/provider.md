---
description: Specifica un provider di traccia (ETW o WPP) per MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118446"
---
# <a name="provider-element"></a>provider (elemento)

Specifica un provider di traccia (ETW o WPP) per [MFTrace.](mftrace.md)

## <a name="usage"></a>Utilizzo

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Attributi



| Attributo            | Type             | Obbligatoria       | Descrizione                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **ID**<br/>    | CDATA<br/> | Sì<br/> | Nome o GUID del provider.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Sì<br/> | Livello di traccia.<br/> <br/>                  |



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

 

 





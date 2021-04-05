---
description: Specifica un provider di traccia (ETW o WPP) per MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753898"
---
# <a name="provider-element"></a>provider (elemento)

Specifica un provider di traccia (ETW o WPP) per [MFTrace](mftrace.md).

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

 

 





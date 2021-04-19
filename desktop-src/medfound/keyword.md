---
description: Specifica una parola chiave per un provider MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento Keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317309"
---
# <a name="keyword-element"></a>elemento Keyword

Specifica una parola chiave per un provider [MFTrace](mftrace.md) .

## <a name="usage"></a>Utilizzo

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Attributi



| Attributo         | Type             | Obbligatoria       | Descrizione                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Sì<br/> | Nome o maschera della parola chiave<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**provider**](provider.md)<br/>   |



## <a name="remarks"></a>Commenti

Per l'elemento [**mfdetours**](mfdetours.md) , le parole chiave valide sono elencate nell'argomento [parole chiave MFTrace](mftrace-keywords.md).

Per l'elemento [**provider**](provider.md) , le parole chiave dipendono dal provider di eventi. È possibile utilizzare l'utilità Wevtutil.exe per elencare le parole chiave per un determinato provider.

## <a name="element-information"></a>Informazioni sull'elemento



|              |     |
|--------------|-----|
| Può essere vuoto | Sì |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione MFTrace](mftrace-configuration-file.md)
</dt> <dt>

[Parole chiave MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 





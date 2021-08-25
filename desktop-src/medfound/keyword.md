---
description: Specifica una parola chiave per un provider MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1f7a648e7861dc8d248141f051e9911c9cb93257f47fee5f2b4d2fd9d5469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827551"
---
# <a name="keyword-element"></a>elemento keyword

Specifica una parola chiave per un provider [MFTrace.](mftrace.md)

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
| [**Provider**](provider.md)<br/>   |



## <a name="remarks"></a>Commenti

Per [**l'elemento mfdetours,**](mfdetours.md) le parole chiave valide sono elencate nell'argomento [Parole chiave MFTrace](mftrace-keywords.md).

Per [**l'elemento provider,**](provider.md) le parole chiave dipendono dal provider di eventi. È possibile usare l'Wevtutil.exe per elencare le parole chiave per un determinato provider.

## <a name="element-information"></a>Informazioni sull'elemento

:::row:::
    :::column:::
        Può essere vuoto
    :::column-end:::
    :::column span="2":::
        Sì
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione di MFTrace](mftrace-configuration-file.md)
</dt> <dt>

[Parole chiave di MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 





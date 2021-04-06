---
title: Determinazione di un tipo di attributo
description: L'attributo systemFlags di un oggetto attributeSchema contiene un set di flag che indicano diverse qualità dell'oggetto attributo, ad esempio se l'attributo è costruito o non replicato.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinazione di un tipo di attributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046522"
---
# <a name="determining-an-attribute-type"></a>Determinazione di un tipo di attributo

L'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) di un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contiene un set di flag che indicano diverse qualità dell'oggetto attributo, ad esempio se l'attributo è costruito o non replicato. Nella tabella seguente sono elencati i flag dell'attributo **systemFlags** che influiscono sul tipo di archiviazione dell'attributo. 

| Valore del flag | Descrizione                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Se questo flag è presente nell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l'attributo non viene replicato. |
| 0x00000004 | Se questo flag è presente nell'attributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , l'attributo viene costruito.    |



 

È possibile creare una stringa di query che può essere usata per eseguire query per attributi costruiti o non replicati. Ad esempio, la stringa di query seguente trova tutti gli oggetti [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) non replicati. Tenere presente che la stringa di query richiede l'equivalente decimale del valore, non l'equivalente esadecimale del valore. Per ulteriori informazioni sull'OID della regola di corrispondenza utilizzato da questa stringa di query, vedere [come specificare i valori di confronto](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



L'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) dell'oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di ogni attributo definisce se un attributo è indicizzato; un attributo indicizzato ha un valore pari a 1, un attributo non indicizzato ha un valore pari a 0. Ad esempio, la stringa di query seguente consente di trovare gli oggetti **attributeSchema** che rappresentano gli attributi indicizzati.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



L'attributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) dell'oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di ogni attributo definisce se un attributo viene replicato nel catalogo globale. Questo attributo ha un valore **true** se l'attributo è un membro del catalogo globale o **false** se gli attributi non sono presenti nel catalogo globale. Ad esempio, la stringa di query seguente esegue la ricerca negli oggetti **attributeSchema** replicati nel catalogo globale.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 
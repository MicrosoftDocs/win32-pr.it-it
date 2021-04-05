---
description: Sono disponibili diverse opzioni per il form richiesto da una query quando si esegue una query su una classe di evento contenente oggetti incorporati. I risultati restituiti dalla query variano a seconda del formato della query utilizzata.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Esecuzione di query su oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755055"
---
# <a name="querying-embedded-objects"></a>Esecuzione di query su oggetti incorporati

Sono disponibili diverse opzioni per il form richiesto da una query quando si esegue una query su una classe di evento contenente oggetti incorporati. I risultati restituiti dalla query variano a seconda del formato della query utilizzata.

## <a name="class-definitions"></a>Definizioni di classe

Nell'esempio seguente vengono illustrate le definizioni di classe utilizzate per le query WQL in questo argomento.

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>Esempio

La query seguente restituisce entrambe le classi incorporate, **E1** ed **E2**, ognuna con **Prop1** e **prop2** popolate con i dati.

`SELECT * FROM MyEvent`

La query seguente restituisce l'oggetto incorporato **E1** , ma senza **Prop1** né **prop2** popolato con i dati.

`SELECT E1 FROM MyEvent`

La query seguente restituisce la classe incorporata **E1** solo con **Prop1** popolati con i dati.

`SELECT E1.Prop1 FROM MyEvent`

La query seguente restituisce entrambe le classi incorporate, **E1** ed **E2**, ognuna con **Prop1** e **prop2** popolate con i dati.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Equivale alla prima query usando l'asterisco ( \* ) invece di specificare ogni oggetto e proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> </dl>

 

 




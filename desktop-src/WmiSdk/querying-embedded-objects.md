---
description: Quando si esegue una query su una classe di evento che contiene oggetti incorporati, sono disponibili diverse opzioni relative al formato di una query. I risultati restituiti dalla query variano a seconda del formato della query in uso.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Esecuzione di query su oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af6e0933ae12bb5867ff2ad446928d1b55f5ee7c2022ec60f53de61a3bd4bb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130913"
---
# <a name="querying-embedded-objects"></a>Esecuzione di query su oggetti incorporati

Quando si esegue una query su una classe di evento che contiene oggetti incorporati, sono disponibili diverse opzioni relative al formato di una query. I risultati restituiti dalla query variano a seconda del formato della query in uso.

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

La query seguente restituisce entrambe le classi incorporate, **E1** **ed E2,** ognuna con **Prop1** e **Prop2** popolate con i dati.

`SELECT * FROM MyEvent`

La query seguente restituisce **l'oggetto incorporato E1,** ma senza **Prop1** né **Prop2** popolati con dati.

`SELECT E1 FROM MyEvent`

La query seguente restituisce la classe incorporata **E1 con** solo **Prop1** popolato con i dati.

`SELECT E1.Prop1 FROM MyEvent`

La query seguente restituisce entrambe le classi incorporate, **E1** **ed E2,** ognuna con **Prop1** e **Prop2** popolate con i dati.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Equivale alla prima query che usa l'asterisco ( \* ) invece di specificare ogni oggetto e proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query con WQL](querying-with-wql.md)
</dt> </dl>

 

 




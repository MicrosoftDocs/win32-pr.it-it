---
description: Gli oggetti dati contengono i dati effettivi o un riferimento a tali dati. Ogni oggetto dati dispone di un modello corrispondente che specifica il tipo di dati. Nelle sezioni seguenti vengono illustrati il form e le parti degli oggetti dati.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Data (formato file X, codifica testo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401248"
---
# <a name="data-x-file-format-text-encoding"></a>Data (formato file X, codifica testo)

Gli oggetti dati contengono i dati effettivi o un riferimento a tali dati. Ogni oggetto dati dispone di un modello corrispondente che specifica il tipo di dati. Nelle sezioni seguenti vengono illustrati il form e le parti degli oggetti dati.

## <a name="form-identifier-and-name"></a>Form, identificatore e nome

Gli oggetti dati hanno il formato seguente.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



L'identificatore è obbligatorio e deve corrispondere a una primitiva o a un tipo di dati definito in precedenza. Il nome è tuttavia facoltativo.

## <a name="data-members"></a>Membri dei dati

I membri dati possono essere uno dei seguenti: oggetto dati, riferimento ai dati, elenco di numeri interi, elenco float o elenco stringhe.

Un oggetto dati è un oggetto dati annidato. Ciò consente di esprimere la natura gerarchica del formato di file. I tipi di oggetti dati annidati consentiti nella gerarchia possono essere limitati.

Un riferimento ai dati è un riferimento a un oggetto dati precedentemente rilevato, come illustrato nell'esempio seguente.


```
{
  name |
  UUID |
  name UUID
}
```



Un elenco di numeri interi è un elenco di numeri interi separato da punti e virgola, come illustrato nell'esempio seguente.


```
1; 2; 3;
```



Un elenco float è un elenco delimitato da punti e virgola di float, come illustrato nell'esempio seguente.


```
1.0; 2.0; 3.0;
```



Un elenco di stringhe è un elenco di stringhe delimitato da punto e virgola, come illustrato nell'esempio seguente.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 




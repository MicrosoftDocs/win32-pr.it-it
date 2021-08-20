---
description: Gli oggetti dati contengono i dati effettivi o un riferimento a questi dati. Ogni oggetto dati ha un modello corrispondente che specifica il tipo di dati. Le sezioni seguenti illustrano il modulo e le parti degli oggetti dati.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Dati (formato di file X, codifica del testo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acd4222e2878b882b8777e3ba22e28f2d213fb5f3550686baf29b4ed6719e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730202"
---
# <a name="data-x-file-format-text-encoding"></a>Dati (formato di file X, codifica del testo)

Gli oggetti dati contengono i dati effettivi o un riferimento a questi dati. Ogni oggetto dati ha un modello corrispondente che specifica il tipo di dati. Le sezioni seguenti illustrano il modulo e le parti degli oggetti dati.

## <a name="form-identifier-and-name"></a>Modulo, identificatore e nome

Gli oggetti dati hanno il formato seguente.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



L'identificatore è obbligatorio e deve corrispondere a un tipo di dati definito in precedenza o a una primitiva. Tuttavia, il nome è facoltativo.

## <a name="data-members"></a>Membri dei dati

I membri dati possono essere uno dei seguenti: oggetto dati, riferimento ai dati, elenco di numeri interi, elenco float o elenco di stringhe.

Un oggetto dati è un oggetto dati annidato. Ciò consente di esprimere la natura gerarchica del formato di file. I tipi di oggetti dati annidati consentiti nella gerarchia possono essere limitati.

Un riferimento ai dati è un riferimento a un oggetto dati rilevato in precedenza, come illustrato nell'esempio seguente.


```
{
  name |
  UUID |
  name UUID
}
```



Un elenco di numeri interi è un elenco di numeri interi separati da punto e virgola, come illustrato nell'esempio seguente.


```
1; 2; 3;
```



Un elenco float è un elenco di valori float separati da punto e virgola, come illustrato nell'esempio seguente.


```
1.0; 2.0; 3.0;
```



Un elenco di stringhe è un elenco di stringhe separate da punto e virgola, come illustrato nell'esempio seguente.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 




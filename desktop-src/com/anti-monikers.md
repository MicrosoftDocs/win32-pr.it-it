---
title: Anti-moniker
description: OLE fornisce un'implementazione di un tipo speciale di moniker denominato anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044853"
---
# <a name="anti-monikers"></a>Anti-moniker

OLE fornisce un'implementazione di un tipo speciale di moniker denominato *anti-moniker*. Questo moniker viene usato nella creazione di nuove classi moniker. Viene usato come inverso del moniker su cui è composto, annullando in modo efficace tale moniker, nello stesso modo in cui l'operatore ".." sposta un livello di directory in un file system comando.

È necessario avere un anti-moniker disponibile perché, una volta creato un moniker composito, non è possibile eliminare parti del moniker se, ad esempio, un oggetto viene spostato. Usare invece un anti-moniker per rimuovere una o più voci da un moniker composito.

Gli anti-moniker sono una classe moniker destinata in modo esplicito all'uso come inverso. COM definisce la funzione [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) denominata, che restituisce un anti-moniker. Questa funzione viene in genere usata per implementare il metodo [**IMoniker:: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .

Un anti-moniker è solo un inverso per i tipi di moniker implementati per considerare gli anti-moniker come inverso. Se ad esempio si vuole rimuovere l'ultima parte di un moniker composito, è consigliabile non creare un anti-moniker e componerlo alla fine del composto. Non è possibile assicurarsi che l'ultima parte del composito consideri un anti-moniker come inverso. Al contrario, è necessario chiamare [**IMoniker:: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) sul moniker composito, specificando **false** come primo parametro. Viene creato un enumeratore che restituisce i moniker dei componenti in ordine inverso. Utilizzare l'enumeratore per recuperare l'ultima parte del composito e chiamare [**inverso**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) su tale moniker. Il moniker restituito da **inverse** è quello necessario per rimuovere l'ultima parte del composto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker della classe](class-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker elemento](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 





---
description: Gli oggetti a protezione diretta utilizzano un formato di maschera di accesso in cui i quattro bit più significativi specificano i diritti di accesso generici.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Diritti di accesso generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758249"
---
# <a name="generic-access-rights"></a>Diritti di accesso generici

Gli oggetti a protezione diretta utilizzano un [formato di maschera di accesso](access-mask-format.md) in cui i quattro bit più significativi specificano i diritti di accesso generici. Ogni tipo di oggetto a protezione diretta esegue il mapping di questi bit a un set di diritti di accesso standard e specifici per gli oggetti. Un oggetto file di Windows, ad esempio, esegue il mapping del \_ bit di lettura generico al \_ controllo Read e sincronizza i diritti di accesso standard e al file \_ leggere i \_ dati, i file di \_ lettura e i diritti di \_ accesso specifici per gli \_ \_ oggetti. Altri tipi di oggetti mappano il \_ bit di lettura generico a qualsiasi set di diritti di accesso appropriato per quel tipo di oggetto.

È possibile usare i diritti di accesso generici per specificare il tipo di accesso necessario quando si apre un handle a un oggetto. Questa operazione è in genere più semplice rispetto a specificare tutti i diritti standard e specifici corrispondenti.

Nella tabella seguente vengono illustrate le costanti definite per i diritti di accesso generici.



| Costante         | Significato generico            |
|------------------|----------------------------|
| tutti GENERIci \_     | Tutti i diritti di accesso possibili |
| esecuzione GENERIca \_ | Esegui accesso             |
| lettura GENERIca \_    | accesso in lettura                |
| scrittura GENERIca \_   | Accesso in scrittura               |



 

Anche le applicazioni che definiscono oggetti a protezione diretta privati possono usare i diritti di accesso generici.

 

 




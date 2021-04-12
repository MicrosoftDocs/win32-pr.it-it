---
description: Tipi di thread del dispenser di risorse COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipi di thread del dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401403"
---
# <a name="com-resource-dispenser-thread-types"></a>Tipi di thread del dispenser di risorse COM+

Le chiamate a un dispenser di risorse COM+ possono avere origine in uno dei seguenti tipi di thread:

-   Thread Apartment (STA)
-   Thread libero (MTA)
-   Thread non COM (applicazione o thread del Garbage Collector di [Gestione dispenser](com--dispenser-manager.md) )

Se un dispenser di risorse non è un oggetto COM, deve essere in grado di gestire le chiamate provenienti da qualsiasi thread in qualsiasi momento. Se un dispenser di risorse è un oggetto COM, l'oggetto COM deve essere registrato con un modello di threading di **entrambi**. Questo consente ai thread STA o MTA di creare e usare il dispenser di risorse senza un cambio di thread.

Se un dispenser di risorse crea e usa un altro oggetto COM (ad esempio, un gestore di risorse out-of-process), il dispenser di risorse potrebbe dover gestire più proxy per questo altro oggetto COM e assicurarsi che le chiamate all'oggetto vengano effettuate usando il proxy appropriato per il thread chiamante. Quando il dispenser di risorse crea questo oggetto, esegue il marshalling e salva il riferimento. Prima di chiamare di nuovo l'oggetto, è necessario eseguire l'unmarshalling per creare un proxy per il thread chiamante.

Potrebbe essere più efficiente memorizzare nella cache questi proxy per thread mantenendo una mappa dall'ID thread a un puntatore proxy. Questa mappa si espande quando si utilizzano nuovi thread nel processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 




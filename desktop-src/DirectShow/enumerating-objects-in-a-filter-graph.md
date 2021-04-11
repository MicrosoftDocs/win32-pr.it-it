---
description: Enumerazione di oggetti in un grafico di filtro
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerazione di oggetti in un grafico di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124407"
---
# <a name="enumerating-objects-in-a-filter-graph"></a>Enumerazione di oggetti in un grafico di filtro

Un'applicazione potrebbe dover individuare un filtro particolare nel grafico del filtro o anche un particolare pin su un filtro. Ad esempio, potrebbe utilizzare un'interfaccia esposta da un filtro specifico. In alternativa, è possibile creare un grafico di filtro specializzato ed è necessario chiamare i metodi sui singoli pin per connettere i filtri. A questo scopo, DirectShow fornisce diversi metodi per l'enumerazione degli oggetti in un grafico di filtro.

Gli enumeratori descritti in questa sezione seguono il formato standard usato dalle interfacce di enumerazione COM. Per ulteriori informazioni, vedere l'argomento "IEnumXXXX" in Platform SDK. Per informazioni sull'enumerazione dei filtri registrati nel computer dell'utente, ma che non sono ancora presenti nel grafico di filtro, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).

Questo articolo contiene gli argomenti seguenti:

-   [Enumerazione dei filtri](enumerating-filters.md)
-   [Enumerazione dei pin](enumerating-pins.md)
-   [Enumerazione dei tipi di supporto](enumerating-media-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 




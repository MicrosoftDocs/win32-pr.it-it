---
description: Rilevamento delle risorse non allocate
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Rilevamento delle risorse non allocate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb356a7e7243c7e6f856a0dfe165440ff0b909545703032a8442bbcced77649d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305241"
---
# <a name="tracking-non-allocated-resources"></a>Rilevamento delle risorse non allocate

Il gestore del dispenser può tenere traccia di una risorsa non in inventario, in base alla conoscenza della durata dell'oggetto. Quando una risorsa rilevata e non allocata viene liberata, viene distrutta e pertanto non restituita all'inventario. Questa modalità di sola traccia per le risorse poco costose da creare ed eliminare è più utile rispetto all'archiviazione nell'inventario. Questa modalità è utile anche per la gestione di un dispenser di memoria o per una risorsa difficile da eseguire l'inventario perché sono presenti troppi tipi diversi.

In modalità di sola traccia, un dispenser di risorse crea direttamente una risorsa richiesta anziché chiedere al gestore del dispenser di allocare una risorsa dall'inventario. Prima di restituire questa risorsa al componente dell'applicazione richiedente, il dispenser di risorse indica al gestore del dispenser di tenere traccia della risorsa. In questo modo, anche se il componente non è in grado di liberare la risorsa, il gestore di dispenser lo farà al termine della durata del componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti del dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 




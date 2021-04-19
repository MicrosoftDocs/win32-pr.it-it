---
description: Rilevamento di risorse non allocate
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Rilevamento di risorse non allocate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305130"
---
# <a name="tracking-non-allocated-resources"></a>Rilevamento di risorse non allocate

Il responsabile del dispenser può tenere traccia di una risorsa che non è in inventario, in base alla conoscenza della durata dell'oggetto. Quando viene liberata, una risorsa rilevata non allocata viene eliminata e pertanto non viene restituita all'inventario. Questa modalità di sola registrazione per le risorse che possono essere create ed eliminate in modo economico è più utile che archiviarle nell'inventario. Questa modalità è utile anche per la gestione di un dispenser di memoria o per una risorsa difficile da inventariare perché sono presenti troppi tipi diversi.

In modalità di sola registrazione, un dispenser di risorse crea direttamente una risorsa richiesta anziché chiedere al responsabile del dispenser di allocarne una dall'inventario. Prima di restituire questa risorsa al componente dell'applicazione richiedente, il dispenser di risorse indica al responsabile del dispenser di tenere traccia della risorsa, garantendo che anche se il componente trascura di liberare la risorsa, il gestore di dispenser lo eseguirà al termine della durata del componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 




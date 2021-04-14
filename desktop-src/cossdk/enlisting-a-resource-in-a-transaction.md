---
description: Integrazione di una risorsa in una transazione
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Integrazione di una risorsa in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401513"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Integrazione di una risorsa in una transazione

Dopo che una risorsa è stata allocata, ma appena prima di restituire la risorsa al dispenser di risorse, il gestore del dispenser verifica con COM+ se l'oggetto chiamante è in esecuzione all'interno di una transazione. Se l'oggetto chiamante è in esecuzione all'interno di una transazione, il gestore del dispenser chiama di nuovo il dispenser di risorse e chiede di integrare la risorsa nella transazione. La risorsa viene quindi restituita al dispenser di risorse, che quindi la restituisce all'istanza chiamante.

Il dispenser di risorse deve essere in grado di integrarsi in una transazione OLE con il Distributed Transaction Coordinator (DTC).

> [!Note]  
> L'integrazione delle transazioni è facoltativa quando un dispenser di risorse distribuisce risorse non transazionali, ad esempio memoria o thread.

 

Quando una transazione viene completata, COM+ notifica al gestore del dispenser se è stato eseguito il commit o l'interruzione. Quindi, il responsabile del dispenser informa il titolare di ogni distributore che le risorse integrate in questa transazione possono ora essere spostate nell'inventario generale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Stati risorse in pool disponibili per il dispenser di risorse COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Processo di allocazione delle risorse del dispenser di risorse](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 




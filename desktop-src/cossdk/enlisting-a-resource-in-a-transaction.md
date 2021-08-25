---
description: Integrazione di una risorsa in una transazione
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Integrazione di una risorsa in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef1ab34d32853be0ca7d4641958b4f57ab55577865aad8612821e98882c71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858961"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Integrazione di una risorsa in una transazione

Dopo l'allocazione di una risorsa, ma subito prima di restituire la risorsa al distributore di risorse, il gestore di dispenser verifica con COM+ se l'oggetto chiamante è in esecuzione all'interno di una transazione. Se l'oggetto chiamante è in esecuzione all'interno di una transazione, il gestore di dispenser chiama di nuovo il distributore di risorse e chiede di integrare la risorsa nella transazione. La risorsa viene quindi restituita al distributore di risorse, che quindi la restituisce all'istanza chiamante.

Il distributore di risorse deve essere in grado di eseguire l'integrazione in una transazione OLE con Distributed Transaction Coordinator (DTC).

> [!Note]  
> L'integrazione delle transazioni è facoltativa quando un dispenser di risorse distribuisce risorse non transazionali, ad esempio memoria o thread.

 

Al termine di una transazione, COM+ notifica al gestore di dispenser se ne è stato eseguito il commit o l'interruzione. Il gestore del distributore notifica quindi al titolare di ogni distributore di risorse che tutte le risorse integrate in questa transazione possono ora essere spostate nell'inventario generale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi ai distributori di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Stati delle risorse in pool disponibili per il dispenser di risorse COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Processo di allocazione delle risorse del distributore di risorse](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 




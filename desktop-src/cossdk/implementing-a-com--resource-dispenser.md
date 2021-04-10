---
description: Implementazione di un dispenser di risorse COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementazione di un dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127550"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementazione di un dispenser di risorse COM+

Nei passaggi seguenti viene illustrata una procedura generale per l'implementazione di un dispenser di risorse COM+:

1.  Decidere il formato **RESTYPID** che categorizza le differenze tra le risorse.

2.  Utilizzare rispettivamente il file di intestazione e la libreria Mtxdm. h e Mtxdm. lib.

3.  Compilare una DLL che implementi l'interfaccia [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e l'API che si vuole esporre alle applicazioni.

4.  Nell'avvio ([*DllMain*](/windows/desktop/Dlls/dllmain) o prima chiamata all'API del dispenser), chiamare la funzione [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) . Viene restituito un puntatore all'interfaccia [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del gestore del dispenser.

5.  Chiamare [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando un puntatore all'implementazione di [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). In questo modo, il responsabile del dispenser crea un contenitore (gestione pool) per il dispenser di risorse e quindi restituisce il puntatore all'interfaccia [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .

6.  Archiviare questo puntatore in modo che sia possibile chiamare [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  È ora possibile (in risposta alle chiamate all'API) effettuare chiamate a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **AllocResource** risponde inizialmente chiamando al metodo [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , ma le chiamate **AllocResource** successive vengono gestite dal pool di risorse in continua crescita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfacce del dispenser di risorse COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 

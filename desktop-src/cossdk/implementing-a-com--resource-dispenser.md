---
description: Implementazione di un dispenser di risorse COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementazione di un dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547893"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementazione di un dispenser di risorse COM+

I passaggi seguenti illustrano una procedura generale per l'implementazione di un distributore di risorse COM+:

1.  Decidere il **formato RESTYPID che** classifica le differenze tra le risorse.

2.  Usare rispettivamente il file di intestazione e la libreria Mtxdm.h e Mtxdm.lib.

3.  Compilare una DLL che implementa [**l'interfaccia IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e l'API da esporre alle applicazioni.

4.  Nell'avvio ([*DllMain*](/windows/desktop/Dlls/dllmain) o prima chiamata all'API dispenser) chiamare la [**funzione GetDispenserManager.**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) Verrà restituito un puntatore all'interfaccia [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del gestore di dispenser.

5.  Chiamare [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando un puntatore all'implementazione di [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). In questo modo il gestore di dispenser crea un titolare (gestore di pooling) per il dispenser di risorse e quindi restituisce il puntatore [**all'interfaccia IHolder.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)

6.  Archiviare questo puntatore in modo che sia possibile chiamare [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  È ora possibile (in risposta alle chiamate all'API) effettuare chiamate a [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **AllocResource** risponde inizialmente chiamando di nuovo il metodo [**CreateResource,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) ma le chiamate **AllocResource** successive vengono gestite dal pool crescente di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi ai distributori di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfacce del distributore di risorse COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 

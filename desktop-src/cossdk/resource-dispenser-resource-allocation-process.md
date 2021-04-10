---
description: Processo di allocazione delle risorse del dispenser di risorse
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processo di allocazione delle risorse del dispenser di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225634"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Processo di allocazione delle risorse del dispenser di risorse

Ogni volta che un dispenser di risorse alloca una risorsa dal relativo titolare, si verifica quanto segue:

1.  Il dispenser di risorse dichiara un identificatore del tipo di risorsa (**RESTYPID**), che descrive il tipo di risorsa necessaria.

2.  Il dispenser di risorse chiama il metodo [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del contenitore, passando questo **RESTYPID**.

3.  Il titolare genera un elenco di candidati dalle risorse disponibili. I candidati sono risorse non integrate in una transazione o già integrate nella transazione dell'oggetto chiamante.

4.  Questi candidati vengono passati singolarmente al metodo [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , in cui vengono classificati (su una scala da 0 a 100) in base alla corrispondenza tra la risorsa candidata e la **RESTYPID** desiderata.

5.  Il titolare sceglie la risorsa che il dispenser di risorse è più alto.

6.  Il dispenser di risorse può terminare il ciclo di classificazione in anticipo assegnando al candidato una valutazione delle risorse 100 (adattamento ottimale). Una classificazione di 100 verrebbe normalmente riservata per le risorse candidate che sono già state integrate correttamente, a meno che il dispenser di risorse non concluda che l'integrazione è un'operazione economica. Se tutte le risorse candidate (se presenti) sono classificate come 0 (inutilizzabile), viene creata una nuova risorsa chiamando [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Se la risorsa scelta in precedenza non è già integrata nella transazione dell'oggetto chiamante, viene chiamato il metodo [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del dispenser di risorse.

8.  La chiamata al metodo [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) restituisce il dispenser di risorse con la risorsa integrata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Integrazione di una risorsa in una transazione](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Rilevamento di risorse non allocate](tracking-non-allocated-resources.md)
</dt> </dl>

 

 




---
description: Processo di allocazione delle risorse del distributore di risorse
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processo di allocazione delle risorse del distributore di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e91802b001bdb8a1af3a933d458c4e9b86b6e3bcd2eb40646e9b64a2e2e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953821"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Processo di allocazione delle risorse del distributore di risorse

Ogni volta che un distributore di risorse alloca una risorsa dal relativo titolare, si verifica quanto segue:

1.  Il dispenser di risorse dichiara un identificatore del tipo di risorsa (**RESTYPID**), che descrive il tipo di risorsa richiesto.

2.  Il dispenser di risorse chiama il metodo [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del titolare, passando **questo RESTYPID**.

3.  Il titolare genera un elenco di candidati dalle risorse disponibili. I candidati sono risorse non integrabili in una transazione o già integrate nella transazione dell'oggetto chiamante.

4.  Questi candidati vengono passati singolarmente al metodo [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) in cui vengono classificati (su una scala da 0 a 100) in base al livello di corrispondenza della risorsa candidata con il **RESTYPID desiderato.**

5.  Il titolare sceglie la risorsa che il distributore di risorse valuta come più alta.

6.  Il distributore di risorse può terminare il ciclo di valutazione in anticipo assegnando al candidato una classificazione delle risorse pari a 100 (una scelta ideale). Una classificazione pari a 100 viene in genere riservata alle risorse candidate già correttamente integrate, a meno che il dispenser di risorse non concluda che l'integrazione è un'operazione economica. Se tutte le risorse candidate (se presenti) sono classificate come 0 (inutilizzabili), viene creata una nuova risorsa chiamando [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Se la risorsa scelta in precedenza non è già integrata nella transazione dell'oggetto chiamante, viene chiamato il metodo [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del dispenser di risorse.

8.  La [**chiamata al metodo AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) restituisce al distributore di risorse con la risorsa integrata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi ai distributori di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Integrazione di una risorsa in una transazione](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Rilevamento di risorse non allocate](tracking-non-allocated-resources.md)
</dt> </dl>

 

 




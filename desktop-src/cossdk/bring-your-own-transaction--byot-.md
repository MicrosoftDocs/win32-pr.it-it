---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305019"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT consente la creazione di un componente con o per ereditare una transazione esterna. Ovvero, un componente che non dispone già di una transazione associata può acquisire una transazione. Attualmente, le transazioni MTS sono automatiche; la presenza di un'istanza del componente in una transazione viene determinata al momento della creazione. Gli attributi transazionali di un componente e il relativo autore determinano la transazione associata a una determinata istanza. In tutti i casi, MTS controlla la durata delle transazioni. COM+ estende questo per consentire l'impostazione di una transazione DTC o TIP preesistente arbitraria come proprietà di transazione del contesto di un nuovo componente. Ciò consente di associare i componenti configurati alle transazioni la cui durata è controllata da un monitor TP, un OTS o un sistema DBMS.

> [!Note]  
> È necessario usare le transazioni BYOT con cautela. In alcune situazioni, possono causare una transazione che si estende su più domini di sincronizzazione, ovvero consentono il parallelismo con una transazione, causando una condizione di deadlock. Le transazioni automatiche, anziché le transazioni BYOT, rappresentano il modello di programmazione preferito per i writer di componenti aziendali.

 

Le interfacce per le transazioni BYOT includono l'interfaccia [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e l'interfaccia [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) . L'interfaccia **ICreateWithTransactionEx** crea un oggetto che è integrato in una transazione manuale. L'interfaccia **ICreateWithTipTransactionEx** crea un oggetto che è integrato in una transazione manuale utilizzando il protocollo di transazione Internet (tip).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Eredità di transazioni manuali](inheriting-manual-transactions.md)
</dt> </dl>

 

 




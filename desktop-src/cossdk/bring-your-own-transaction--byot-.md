---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308664"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT consente di creare un componente con o ereditare una transazione esterna. Ciò significa che un componente a cui non è già associata una transazione può acquisire una transazione. Attualmente, le transazioni MTS sono automatiche. se un'istanza del componente si trova in una transazione viene determinata al momento della creazione. Gli attributi transazionali di un componente e del relativo autore determinano quale transazione è associata a una determinata istanza. In tutti i casi, MTS controlla la durata delle transazioni. COM+ estende questa funzionalità per consentire l'impostazione di una transazione DTC o TIP preesiste arbitraria come proprietà della transazione del contesto di un nuovo componente. In questo modo i componenti configurati possono essere associati alle transazioni le cui durate sono controllate da un monitoraggio TP, OTS o DBMS.

> [!Note]  
> Le transazioni BYOT devono essere usate con cautela. In determinate situazioni, possono comportare una transazione che si estende su più domini di sincronizzazione, ovvero consentono il parallelismo con una transazione, causando una condizione di deadlock. Le transazioni automatiche, anziché le transazioni BYOT, sono il modello di programmazione preferito per i writer di componenti aziendali.

 

Le interfacce per le transazioni BYOT includono [**l'interfaccia ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**l'interfaccia ICreateWithTipTransactionEx.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) **L'interfaccia ICreateWithTransactionEx** crea un oggetto che viene elencato all'interno di una transazione manuale. **L'interfaccia ICreateWithTipTransactionEx** crea un oggetto che viene incorporato all'interno di una transazione manuale usando il protocollo TIP (Transaction Internet Protocol).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Eredità di transazioni manuali](inheriting-manual-transactions.md)
</dt> </dl>

 

 




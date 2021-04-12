---
description: COM+ offre agli sviluppatori maggiore controllo sulle applicazioni, consentendo livelli di isolamento delle transazioni configurabili.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Configurazione di livelli di isolamento delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483053"
---
# <a name="configuring-transaction-isolation-levels"></a>Configurazione di livelli di isolamento delle transazioni

COM+ offre agli sviluppatori maggiore controllo sulle applicazioni, consentendo livelli di isolamento delle transazioni configurabili. Le versioni di COM+ precedenti a COM+ 1,5 utilizzavano sempre il livello massimo di isolamento per le transazioni. Sebbene questo livello garantisca che l'integrità dei dati venga sempre mantenuta, può causare problemi di prestazioni, ad esempio i timeout, quando è necessario eseguire molte transazioni su un database di grandi dimensioni. Con i livelli di isolamento configurabili, gli sviluppatori esperti possono aumentare la concorrenza per migliorare le prestazioni e la scalabilità.

COM+ fornisce i livelli di isolamento delle transazioni seguenti.



| Level            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serializzato       | I dati letti da una transazione corrente non possono essere modificati da un'altra transazione fino al termine della transazione corrente. Non è possibile inserire nuovi dati che potrebbero influire sulla transazione corrente. Si tratta del livello di isolamento più sicuro ed è il valore predefinito.                                                                                                                                                                                                                                                                                                                                                    |
| Repeatable Read  | I dati letti da una transazione corrente non possono essere modificati da un'altra transazione fino al termine della transazione corrente. Durante una transazione è possibile inserire qualsiasi tipo di dati nuovi.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Read Committed   | Una transazione non è in grado di leggere i dati modificati da un'altra transazione di cui non è stato eseguito il commit. Questo è il livello di isolamento predefinito in Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Read Uncommitted | Una transazione può leggere tutti i dati, anche se vengono modificati da un'altra transazione. Si tratta del livello di isolamento meno sicuro ma consente la concorrenza più elevata.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Qualsiasi              | Qualsiasi livello di isolamento è supportato. Questa impostazione viene usata più di frequente dai componenti downstream per evitare conflitti. Questa impostazione è utile perché qualsiasi componente downstream deve essere configurato con un livello di isolamento uguale o inferiore al livello di isolamento del componente a Monte immediato. Pertanto, un componente downstream con il relativo livello di isolamento configurato come any utilizza sempre lo stesso livello di isolamento utilizzato dal componente a Monte immediato. Se l'oggetto radice in una transazione dispone del livello di isolamento configurato su Any, il relativo livello di isolamento viene serializzato. |



 

> [!Note]  
> Se un componente downstream è configurato con un livello di isolamento superiore rispetto a un componente a Monte e tenta di eseguire l'integrazione in una transazione, viene restituito un errore e la transazione viene interrotta.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione del livello di isolamento delle transazioni](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 




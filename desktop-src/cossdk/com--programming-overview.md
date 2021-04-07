---
description: COM+ fornisce un ambiente di sviluppo aziendale, basato su Microsoft Component Object Model (COM), per la creazione di applicazioni distribuite basate su componenti.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Panoramica della programmazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c225b5ebb6f04f74d6071dc0305d219993fa606e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748074"
---
# <a name="com-programming-overview"></a>Panoramica della programmazione COM+

COM+ fornisce un ambiente di sviluppo aziendale, basato su Microsoft Component Object Model (COM), per la creazione di applicazioni distribuite basate su componenti. Fornisce inoltre gli strumenti per creare applicazioni transazionali multilivello. COM+ combina i miglioramenti allo sviluppo tradizionale basato su COM con molti servizi di programmazione e amministrazione utili. Per un elenco completo di questi servizi, vedere [servizi com+](com--services.md) .

I miglioramenti apportati a COM includono miglioramenti per Threading e sicurezza, oltre all'introduzione dei servizi di sincronizzazione. I servizi includono lo strumento di amministrazione Servizi componenti.

Per coloro che hanno familiarità con la programmazione COM, i miglioramenti COM+ sono significativi, inclusi i seguenti:

-   COM+ implementa un modello di threading denominato Threading Apartment neutro, che consente a un componente di avere l'accesso serializzato insieme alla possibilità di esecuzione su qualsiasi thread.
-   COM+ supporta componenti con un ambiente speciale denominato [contesto](com--contexts.md), che fornisce un set estensibile di proprietà che definiscono l'ambiente di esecuzione per il componente.
-   COM+ fornisce sicurezza basata sui ruoli, esecuzione asincrona degli oggetti e un moniker incorporato che rappresenta un riferimento a un'istanza dell'oggetto in esecuzione in un server out-of-process.

## <a name="application-and-component-administration"></a>Amministrazione di applicazioni e componenti

In COM+, un database di registrazione, denominato RegDB, archivia i metadati che descrivono i componenti. Questo database è altamente ottimizzato per il tipo di informazioni richieste da COM+ per l'attivazione dei componenti e viene utilizzato al posto del registro di sistema. Inoltre, COM+ espone il *Catalogo com+*, che accede alle informazioni in regdb. Il catalogo COM+ è un archivio dati di sistema che contiene informazioni di configurazione per le applicazioni COM+ in un determinato computer server.

Infine, lo strumento di amministrazione Servizi componenti fornisce un'interfaccia utente completamente gestibile da script per gli sviluppatori e gli amministratori per l'amministrazione di componenti, nonché per la distribuzione di applicazioni multilivello sul lato client e sul lato server. Per ulteriori informazioni, vedere [Deploying com+ Applications](deploying-com--applications.md).

## <a name="automatic-transactions"></a>Transazioni automatiche

COM+ supporta la semantica di Microsoft Transaction Server (MTS) 2,0 e aggiunge la funzionalità di [completamento automatico](enabling-auto-done-for-a-method.md) , che è possibile impostare utilizzando lo strumento di amministrazione Servizi componenti. Questa funzionalità consente al sistema di interrompere automaticamente una transazione se viene generata un'eccezione o se non viene eseguito il commit. Per ulteriori informazioni, vedere [transazioni com+](com--transactions.md)e [attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md).

 

 




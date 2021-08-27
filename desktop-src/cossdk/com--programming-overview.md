---
description: COM+ offre un ambiente di sviluppo aziendale, basato su Microsoft Component Object Model (COM), per la creazione di applicazioni distribuite basate su componenti.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Cenni preliminari sulla programmazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421fd6a52eade351eaab09ececff8fc63cc687002dede350ab9f06fa0b2c20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096891"
---
# <a name="com-programming-overview"></a>Cenni preliminari sulla programmazione COM+

COM+ offre un ambiente di sviluppo aziendale, basato su Microsoft Component Object Model (COM), per la creazione di applicazioni distribuite basate su componenti. Offre anche gli strumenti per creare applicazioni transazionali multilivello. COM+ combina miglioramenti allo sviluppo tradizionale basato su COM con molti utili servizi di programmazione e amministrazione. Per [un elenco completo di](com--services.md) questi servizi, vedere Servizi COM+.

I miglioramenti COM includono miglioramenti per il threading e la sicurezza, oltre all'introduzione dei servizi di sincronizzazione. I servizi includono lo strumento di amministrazione Servizi componenti.

Per gli utenti che hanno familiarità con la programmazione COM, i miglioramenti di COM+ sono significativi, inclusi i seguenti:

-   COM+ implementa un modello di threading denominato threading apartment neutro, che consente a un componente di avere accesso serializzato insieme alla possibilità di eseguire su qualsiasi thread.
-   COM+ supporta componenti con un ambiente speciale denominato contesto [,](com--contexts.md)che fornisce un set estendibile di proprietà che definiscono l'ambiente di esecuzione per il componente.
-   COM+ fornisce la sicurezza basata sui ruoli, l'esecuzione asincrona degli oggetti e un moniker predefinito che rappresenta un riferimento a un'istanza di oggetto in esecuzione in un server out-of-process.

## <a name="application-and-component-administration"></a>Amministrazione di applicazioni e componenti

In COM+, un database di registrazione, denominato RegDB, archivia i metadati che descrivono i componenti. Questo database è altamente ottimizzato per il tipo di informazioni necessarie a COM+ per l'attivazione dei componenti e viene usato al posto del Registro di sistema. COM+ espone anche il *catalogo COM+,* che accede alle informazioni in RegDB. Il catalogo COM+ è un archivio dati di sistema che contiene informazioni di configurazione per le applicazioni COM+ in un determinato computer server.

Infine, lo strumento di amministrazione Servizi componenti offre un'interfaccia utente completamente gestibile da script per sviluppatori e amministratori per amministrare i componenti, nonché distribuire applicazioni multitier lato client e lato server. Per altre informazioni, vedere [Distribuzione di applicazioni COM+.](deploying-com--applications.md)

## <a name="automatic-transactions"></a>Transazioni automatiche

COM+ supporta tutta la semantica di Microsoft Transaction Server (MTS) 2.0 e aggiunge la funzionalità di completamento automatico, che è possibile impostare usando lo strumento amministrativo Servizi componenti. [](enabling-auto-done-for-a-method.md) Questa funzionalità consente al sistema di interrompere automaticamente una transazione se viene attivata un'eccezione o di eseguire il commit in caso di errore. Per altre informazioni, vedere [Transazioni COM+](com--transactions.md)e [Attivazione JUST-In-Time COM+.](com--just-in-time-activation.md)

 

 




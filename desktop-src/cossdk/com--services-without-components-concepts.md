---
description: In COM+ 1,5 è stata introdotta la possibilità di utilizzare i servizi COM+ senza componenti.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Concetti relativi ai servizi COM+ senza componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878198"
---
# <a name="com-services-without-components-concepts"></a>Concetti relativi ai servizi COM+ senza componenti

In COM+ 1,5 è stata introdotta la possibilità di utilizzare i servizi COM+ senza componenti. Questo consente di ridurre significativamente i costi di prestazioni quando si utilizzano i servizi COM+ da un ambiente che non utilizza i componenti di e viene eliminata anche la complessità dell'utilizzo di questi servizi. A partire da IIS 6,0, IIS e ASP sfruttano i vantaggi dell'utilizzo di servizi COM+ senza componenti.

I servizi COM+ sono stati originariamente progettati per essere utilizzati con i componenti COM+. Tuttavia, alcuni ambienti di programmazione non sono basati su componenti e pertanto richiedono un sovraccarico sostanziale per l'utilizzo dei servizi COM+. Ad esempio, prima del rilascio di COM+ 1,5, IIS doveva creare oggetti shim esclusivamente per poter utilizzare i servizi di transazione COM+ nelle pagine ASP. I costi di prestazioni derivanti dalla creazione di tali oggetti includono l'archiviazione dei dati di configurazione sia nella metabase IIS che nel database di registrazione COM+ (RegDB), nonché nella comunicazione aggiuntiva tra la metabase IIS e il RegDB COM+ necessario per gestire efficacemente i dati di configurazione.

Se IIS avesse dovuto usare un secondo servizio COM+, ad esempio la sincronizzazione, doveva creare un oggetto shim completamente diverso a tale scopo. Per utilizzare le transazioni COM+ e la sincronizzazione, è necessario un terzo tipo di oggetto shim. La complessità di questo approccio è scalabile come O (N2), rendendo estremamente difficile l'implementazione di nuovi servizi.

Con l'introduzione dei servizi COM+ senza componenti, i servizi necessari vengono configurati tramite un oggetto di cui è stata creata un'istanza dalla classe. La classe [**CServiceConfig**](cserviceconfig.md) implementa le interfacce necessarie per configurare i diversi servizi, garantendo allo stesso tempo la flessibilità necessaria per supportare più servizi e la possibilità di supportare nuovi servizi in futuro.

I servizi configurati possono quindi essere usati attraverso due meccanismi diversi: possono essere usati tramite la funzione [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , che applica i servizi a tutto il lavoro inviato tramite l'attività creata dalla funzione e può essere usato anche incorporando il lavoro che usa i servizi tra le chiamate alle funzioni [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) . Nessuna di queste funzioni richiede la creazione di nuovi componenti per poter utilizzare i servizi COM+. è necessario solo l'oggetto [**CServiceConfig**](cserviceconfig.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi COM+ senza attività componenti](com--services-without-components-tasks.md)
</dt> </dl>

 

 




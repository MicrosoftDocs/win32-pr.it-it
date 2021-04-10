---
description: Creazione di un filtro editore
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Creazione di un filtro editore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997fe37cf0021bcb2aa153c2dc4b73597e0c43cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127555"
---
# <a name="creating-a-publisher-filter"></a>Creazione di un filtro editore

Esistono due metodi per stabilire il filtro del server di pubblicazione: utilizzando la proprietà MultiPublisherFilterCLSID della classe di evento o utilizzando [**IEventControl:: SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Poiché consente di comporre l'oggetto evento con il servizio [componenti in coda com+](com--queued-components.md) , il metodo preferito consiste nell'usare la proprietà MultiPublisherFilterCLSID nella classe di evento per impostare il filtro del server di pubblicazione. Viene stabilito un oggetto filtro per tutti i metodi delle interfacce evento per un oggetto evento. L'oggetto evento attiva il filtro del server di pubblicazione quando viene creata un'istanza dell'oggetto classe di evento utilizzando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   È anche possibile usare [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter). Tuttavia, se si sceglie questo metodo, l'interfaccia non è accodabile e pertanto non può utilizzare l'oggetto evento con il servizio componenti in coda COM+ tra il server di pubblicazione e l'oggetto classe di evento. Per ulteriori informazioni sull'utilizzo del servizio componenti in coda con eventi COM+, vedere [utilizzo di eventi com+ con componenti in coda com+](using-com--events-with-com--queued-components.md).

Un evento può contenere uno o più oggetti filtro o nessuno. Gli oggetti filtro del server di pubblicazione devono supportare [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) o [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter), a seconda che si disponga di una singola interfaccia di attivazione o di più interfacce di attivazione nell'oggetto classe di evento. Le interfacce **IPublisherFilter** e **IMultiInterfacePublisherFilter** specificano entrambe un metodo **Initialize** . Il metodo **Initialize** viene chiamato dall'oggetto della classe di evento immediatamente dopo la creazione dell'oggetto Filter.

Gli eventi COM+ tentano di richiamare due metodi sul filtro. In primo luogo chiama [**IPublisherFilter::P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) e passa un puntatore di interfaccia [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) al filtro. Viene quindi eseguita una query sull'oggetto filtro per l'interfaccia evento. Se il filtro supporta l'interfaccia evento, richiama un metodo su di esso. Ciò consente di accedere ai parametri del server di pubblicazione per un evento. Il filtro può usare questi parametri per determinare le sottoscrizioni da attivare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 

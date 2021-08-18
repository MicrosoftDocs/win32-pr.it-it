---
description: Creazione di un Publisher filtro
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Creazione di un Publisher filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2cf3391cd331f7d81c3bb7ff467c140a78b0c8e30fb609ea655596dfe745a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128793"
---
# <a name="creating-a-publisher-filter"></a>Creazione di un Publisher filtro

Esistono due metodi per stabilire il filtro del server di pubblicazione: usando la proprietà MultiPublisherFilterCLSID della classe di evento o [**IEventControl::SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Poiché consente di comporre l'oggetto evento con il servizio componenti in coda [COM+,](com--queued-components.md) il metodo preferito è usare la proprietà MultiPublisherFilterCLSID nella classe di evento per impostare il filtro del server di pubblicazione. In questo modo viene stabilito un oggetto filtro per tutti i metodi delle interfacce eventi per un oggetto evento. L'oggetto evento attiva il filtro del server di pubblicazione quando viene creata un'istanza dell'oggetto della classe di evento usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   È anche possibile usare [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter). Tuttavia, se si sceglie questo metodo, l'interfaccia non è accodamentabile e pertanto non può usare l'oggetto evento con il servizio componenti in coda COM+ tra il server di pubblicazione e l'oggetto della classe di evento. Per altre informazioni sull'uso del servizio componenti in coda con eventi COM+, vedere Uso di eventi COM+ con componenti in coda [COM+.](using-com--events-with-com--queued-components.md)

Un evento può avere uno o più oggetti filtro o nessuno. Gli oggetti filtro dell'editore devono supportare [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) o [**IMultiInterfacePublisherFilter,**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)a seconda che si abbia una singola interfaccia di attivazione o più interfacce di attivazione nell'oggetto della classe di evento. Entrambe **le interfacce IPublisherFilter** e **IMultiInterfacePublisherFilter** specificano un **metodo Initialize.** Il **metodo Initialize** viene chiamato dall'oggetto classe di evento immediatamente dopo la creazione dell'oggetto filtro.

Gli eventi COM+ tentano di richiamare due metodi sul filtro. Prima chiama [**IPublisherFilter::P repareToFire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) e passa un puntatore a interfaccia [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) al filtro. Esegue quindi una query sull'oggetto filtro per l'interfaccia eventi. Se il filtro supporta l'interfaccia eventi, richiama un metodo su di essa. In questo modo è possibile accedere ai parametri del server di pubblicazione per un evento. Il filtro può usare questi parametri per determinare le sottoscrizioni da impostare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione di filtri agli eventi in COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 

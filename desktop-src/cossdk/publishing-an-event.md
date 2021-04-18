---
description: Pubblicazione di un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Pubblicazione di un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304938"
---
# <a name="publishing-an-event"></a>Pubblicazione di un evento

Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto evento chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o il metodo **CreateObject** di Microsoft Visual Basic usando EventClassID o EventClassName come argomento. Il server di pubblicazione chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto evento per ottenere le interfacce supportate dall'oggetto della classe di evento e richiama un metodo sull'oggetto evento tramite l'interfaccia per pubblicare l'evento. Il sistema di eventi pubblica quindi gli eventi nella classe di evento CLSID \_ EventObjectChange con l'ID di interfaccia IID \_ IEventObjectChange.

Per supportare il recapito di eventi a più sottoscrittori, i metodi della classe di evento devono contenere solo parametri in.

Utilizzando la proprietà FireInParallel dell'oggetto [classe di evento](the-com--event-class-object.md) , i publisher possono richiedere che il sistema di eventi utilizzi più thread per recapitare un evento a più Sottoscrittori. La selezione di un meccanismo di recapito in parallelo non garantisce il recapito simultaneo dell'evento a più sottoscrittori, ma indica al servizio eventi COM+ di consentire questo problema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 

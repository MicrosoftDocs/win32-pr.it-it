---
description: Pubblicazione di un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Pubblicazione di un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724dc94ddf9cc25ec3b11cc31376805241e9d6d67250f8a494f8b417b9d201a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990501"
---
# <a name="publishing-an-event"></a>Pubblicazione di un evento

Per pubblicare un evento, è sufficiente creare un'istanza di un oggetto evento chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o il metodo **CreateObject** di Microsoft Visual Basic usando EventClassID o EventClassName come argomento. Il server di pubblicazione chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto evento per ottenere le interfacce supportate dall'oggetto classe di evento e richiama un metodo sull'oggetto evento tramite l'interfaccia per pubblicare l'evento. Il sistema di eventi pubblica quindi gli eventi nella classe di evento CLSID \_ EventObjectChange con l'ID di interfaccia IID \_ IEventObjectChange.

Per supportare il recapito di eventi a più sottoscrittori, i metodi della classe di evento devono contenere solo nei parametri.

Usando la proprietà FireInParallel [](the-com--event-class-object.md) dell'oggetto classe di evento, gli editori possono richiedere che il sistema di eventi usi più thread per recapitare un evento a più sottoscrittori. La selezione di un meccanismo di recapito in parallelo non garantisce il recapito simultaneo dell'evento a più sottoscrittori, ma indica al servizio eventi COM+ di consentire questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pubblicazione e recapito di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 

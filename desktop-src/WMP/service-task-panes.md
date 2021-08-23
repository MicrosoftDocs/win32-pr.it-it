---
title: Riquadri attività Servizio
description: Riquadri attività Servizio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player negozi online, riquadri attività servizio
- negozi online, riquadri attività servizio
- tipo 2 negozi online, riquadri attività servizio
- Windows Media Player online, riquadri attività
- negozi online, riquadri attività
- tipo 2 negozi online, riquadri attività
- Windows Media Player,riquadri attività Servizio
- Windows Media Player,riquadri attività
- riquadri attività del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646511"
---
# <a name="service-task-panes"></a>Riquadri attività Servizio

In Windows Media Player 10, i provider di punti vendita online possono configurare Windows Media Player visualizzare fino a tre riquadri attività, denominati riquadri attività di servizio. Ogni riquadro attività del servizio è rappresentato da un pulsante personalizzabile Windows Media Player visualizzato sul lato destro della barra delle applicazioni Funzionalità.

Ogni riquadro attività del servizio ospita una pagina Web che rappresenta l'interfaccia utente per una particolare funzionalità del negozio online. L'aspetto dei riquadri attività del servizio è definito dal documento XML ServiceInfo. In questo documento i riquadri attività del servizio sono rappresentati da tre elementi: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**. Questi riquadri attività del servizio hanno lo scopo di fornire quanto segue:

-   Un servizio di musica.
-   Un servizio video.
-   Un servizio radio.

È possibile posizionare queste funzionalità in Windows Media Player nell'ordine in cui si desidera, ma **ServiceTask1** deve essere il riquadro attività principale per l'attività commerciale.

La pagina Web ospitata in ogni riquadro attività del servizio ha accesso **all'oggetto** Esterno. Questo oggetto fornisce metodi, proprietà e un evento che forniscono funzionalità speciali per le pagine Web Windows Media Player. Ad esempio, è possibile usare  l'evento e le proprietà di External per fare in modo che l'aspetto della pagina Web corrisponda alla combinazione di colori scelta dall'utente per Windows Media Player.

Nella Windows Media Player 11 non sono presenti riquadri attività di servizio. È invece disponibile una singola scheda **Online Stores,** che ospita la pagina Web principale per il negozio online attivo. Nel documento ServiceInfo la **scheda Online Stores** è rappresentata dall'elemento **ServiceTask1.** Gli **elementi ServiceTask2** **e ServiceTask3** vengono ignorati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Oggetto esterno per i negozi online di tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo per un Negozio online di tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 





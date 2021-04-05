---
description: Un provider di eventi deve implementare l'interfaccia IWbemEventProvider per generare notifiche degli eventi.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967971"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implementazione dell'interfaccia primaria per un provider di eventi

Un provider di eventi deve implementare l'interfaccia [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) per generare notifiche degli eventi. WMI chiama il metodo [**IWbemEventProvider::P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) del provider e passa un puntatore all'oggetto sink, che è un'implementazione dell'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) . Quando il provider di eventi è pronto per generare una notifica, il provider chiama il metodo [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Un provider di eventi deve inserire le notifiche generate tramite [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) negli oggetti evento. È necessario implementare oggetti evento come voci in una matrice di interfacce [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) rappresentate dal parametro *PpObjArray* del metodo [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . Poiché **IWbemClassObjects** sono oggetti com, il provider deve incrementare il conteggio dei riferimenti per il sink chiamando il metodo [**IWbemObjectSink:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . I provider di eventi che devono fornire molte notifiche, ad esempio 400 eventi, devono creare un oggetto evento univoco per ogni notifica generando una nuova istanza o clonando una esistente. WMI non contiene mai un oggetto evento oltre il completamento della chiamata di **indicazione** e non ha requisiti speciali per **AddRef** oltre lo standard com.

Quando si implementa un provider di eventi, tenere presenti le linee guida seguenti:

-   Non apportare modifiche alle classi durante la manutenzione di una chiamata client.
-   Non eseguire chiamate relative agli eventi, ad esempio una chiamata che modifica un filtro eventi.
-   Elaborare qualsiasi richiesta rilasciata dal servizio di gestione di Windows, ad esempio [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery), prima di riattivare un evento.

    Se non si elabora la richiesta, la rigenerazione dell'evento potrebbe impedire che l'evento venga mai accettato.

-   Non chiamare mai [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) dall'interno di un provider.

 

 

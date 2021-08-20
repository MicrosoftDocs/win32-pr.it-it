---
description: Un provider di eventi deve implementare l'interfaccia IWbemEventProvider per generare notifiche degli eventi.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5847f14cbe9f27460ee1477d9b76d725db7769fa147a9fd18bf275e587014e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108585"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implementazione dell'interfaccia primaria per un provider di eventi

Un provider di eventi deve implementare [**l'interfaccia IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) per generare notifiche degli eventi. WMI chiama il [**metodo IWbemEventProvider::P rovideEvents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) del provider e passa un puntatore all'oggetto sink, che è un'implementazione dell'interfaccia [**IWbemObjectSink.**](iwbemobjectsink.md) Quando il provider di eventi è pronto per generare una notifica, chiama il [**metodo IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

Un provider di eventi deve inserire le notifiche generate tramite [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) negli oggetti evento. È necessario implementare gli oggetti evento come voci in una matrice di interfacce [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) rappresentate dal *parametro ppObjArray* del [**metodo Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Poiché **IWbemClassObjects** è un oggetto COM, il provider deve incrementare il conteggio dei riferimenti per il sink chiamando il [**metodo IWbemObjectSink::AddRef.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) I provider di eventi che devono fornire molte notifiche (ad esempio, 400 eventi) devono creare un oggetto evento univoco per ogni notifica generando una nuova istanza o clonando un oggetto esistente. WMI non mantiene mai un oggetto evento dopo il completamento della chiamata **Indicate** e non ha requisiti speciali per **AddRef** sopra e oltre lo standard COM.

Quando si implementa un provider di eventi, tenere presenti le linee guida seguenti:

-   Non apportare modifiche alla classe durante la manutenzione di una chiamata client.
-   Non eseguire chiamate correlate a eventi, ad esempio una chiamata che modifica un filtro eventi.
-   Elaborare le richieste che il Windows Management, ad esempio [**CancelQuery,**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery)prima di riasferire un evento.

    Se non si elabora la richiesta, l'aggiornamento dell'evento potrebbe impedire l'accettazione dell'evento.

-   Non chiamare [**mai IWbemObjectSink::SetStatus dall'interno**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) di un provider.

 

 

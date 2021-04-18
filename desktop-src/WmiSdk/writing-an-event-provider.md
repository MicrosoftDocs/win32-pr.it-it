---
description: Un provider di eventi è un oggetto COM che fornisce WMI con notifiche di eventi intrinseci ed estrinseci.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Scrittura di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310315"
---
# <a name="writing-an-event-provider"></a>Scrittura di un provider di eventi

Un provider di eventi è un oggetto COM che fornisce WMI con notifiche di eventi intrinseci ed estrinseci. Un evento intrinseco segnala una modifica interna dei dati in WMI, mentre un evento estrinseco segnala un evento definito dall'utente non descritto da un evento intrinseco. Ad esempio, un evento in risposta a modifiche, creazione o eliminazione della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) verrebbe classificato come un evento intrinseco. Un evento generato in base a elementi diversi dalla modifica, creazione o eliminazione di un oggetto WMI esistente è un evento estrinseco. Indipendentemente dalla classe supportata, è possibile implementare tutti i provider di eventi nello stesso modo.

Nella procedura riportata di seguito viene descritto come implementare un provider di eventi.

**Per implementare un provider di eventi**

1.  Progettare e registrare il provider di classi con WMI.

    I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di eventi](registering-an-event-provider.md).

2.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    L'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) è un'interfaccia comune utilizzata da WMI per caricare e inizializzare tutti i provider. Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).

3.  Implementare [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) come interfaccia principale per il provider.

    L'interfaccia [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) usa il metodo **ProviderEvents** per fornire eventi a WMI. Per ulteriori informazioni, vedere [Implementing the primary interface for a event provider](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > I provider di eventi devono usare il modello di multithreading "both".

     

4.  Facoltativamente, è anche possibile implementare l'interfaccia [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) per migliorare le prestazioni del provider di eventi.

    L'interfaccia [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) consente al provider di ottimizzare le query prima di inviare una risposta a WMI ed è particolarmente utile per un provider che fornisce eventi di più tipi e che deve eseguire il maggior numero possibile di ottimizzazioni interne. Per ulteriori informazioni, vedere [ottimizzazione di un provider di eventi](optimizing-an-event-provider.md).

5.  Implementare l'interfaccia [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) per limitare gli utenti a determinati ID di sicurezza (SID) o implementare [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) per proteggere il sink stesso. Il provider può inoltre impostare la proprietà del **\_ descrittore di sicurezza** nella classe di evento per proteggere i singoli eventi nel codice MOF. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).
6.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

7.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia. Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).

Un'applicazione client può richiedere un evento registrandosi con WMI come consumer di eventi. Per ulteriori informazioni, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

 

 

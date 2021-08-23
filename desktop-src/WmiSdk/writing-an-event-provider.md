---
description: Un provider di eventi è un oggetto COM che fornisce a WMI notifiche di eventi intrinseci ed estensivi.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Scrittura di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04abf060ef5316790b04682430abd92d0a6bea31175f0e192fc7f73d047633d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757211"
---
# <a name="writing-an-event-provider"></a>Scrittura di un provider di eventi

Un provider di eventi è un oggetto COM che fornisce a WMI notifiche di eventi intrinseci ed estensivi. Un evento intrinseco segnala una modifica dei dati interni a WMI, mentre un evento estensiva segnala un evento definito dall'utente non descritto da un evento intrinseco. Ad esempio, un evento in risposta a modifiche, creazione o eliminazione della [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) verrebbe classificato come evento intrinseco. Un evento generato in base a un elemento diverso dalla modifica, dalla creazione o dall'eliminazione di un oggetto WMI esistente è un evento estensiva. Indipendentemente dalla classe supportata, è possibile implementare tutti i provider di eventi nello stesso modo.

La procedura seguente descrive come implementare un provider di eventi.

**Per implementare un provider di eventi**

1.  Progettare e registrare il provider di classi con WMI.

    I provider di classi si registrano con WMI creando [**\_ \_ un'istanza win32Provider**](--win32provider.md) e una [**\_ \_ classe EventProviderRegistration.**](--eventproviderregistration.md) Per altre informazioni, vedere [Registrazione di un provider di eventi](registering-an-event-provider.md).

2.  Implementare [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    [**L'interfaccia IWbemProviderInit è**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) un'interfaccia comune utilizzata da WMI per caricare e inizializzare tutti i provider. Per altre informazioni, vedere [Inizializzazione di un provider](initializing-a-provider.md).

3.  Implementare [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) come interfaccia primaria per il provider.

    [**L'interfaccia IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) usa il **metodo ProviderEvents** per fornire eventi a WMI. Per altre informazioni, vedere [Implementazione dell'interfaccia primaria per un provider di eventi](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > I provider di eventi devono usare il modello di multithreading "Both".

     

4.  Facoltativamente, è anche possibile implementare [**l'interfaccia IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) per aumentare le prestazioni del provider di eventi.

    [**L'interfaccia IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) consente al provider di ottimizzare le query prima di inviare una risposta a WMI ed è particolarmente utile per un provider che fornisce eventi di più tipi e che deve eseguire il maggior numero possibile di ottimizzazioni interne. Per altre informazioni, vedere [Ottimizzazione di un provider di eventi](optimizing-an-event-provider.md).

5.  Implementare [**l'interfaccia IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) per limitare i consumer a determinati identificatori di sicurezza (SID) o [**implementare IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) per proteggere il sink stesso. Il provider può anche impostare la **proprietà SECURITY \_ DESCRIPTOR** nella classe di evento per proteggere singoli eventi nel codice MOF. Per altre informazioni, vedere [Protezione degli eventi WMI](securing-wmi-events.md).
6.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per tale client. Per altre informazioni, vedere [Rappresentazione di un client](impersonating-a-client.md).

7.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente su cui eseguire la copia. Per altre informazioni, vedere [Aggiornamento di un provider](updating-a-provider.md).

Un'applicazione client può richiedere un evento registrando se stessa con WMI come consumer di eventi. Per altre informazioni, vedere [Ricezione di un evento WMI.](receiving-a-wmi-event.md)

 

 

---
description: Un provider di consumer di eventi è un componente dell'architettura del consumer permanente che determina il consumer di eventi permanente che gestisce un determinato evento.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Scrittura di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313676"
---
# <a name="writing-an-event-consumer-provider"></a>Scrittura di un provider di consumer di eventi

Un provider di consumer di eventi è un componente dell'architettura del consumer permanente che determina il consumer di eventi permanente che gestisce un determinato evento. È necessario creare un provider di consumer di eventi insieme ai consumer di eventi permanenti per indirizzare correttamente gli eventi da WMI.

Un provider di consumer di eventi collega un provider di eventi a un elenco di classi consumer. Le istanze di queste classi consumer ricevono quindi gli eventi da tale provider. WMI identifica il provider di consumer a cui vengono recapitati gli eventi, in base all'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , che associa l'istanza [**\_ \_ Win32Provider**](--win32provider.md) del provider consumer a una classe consumer logica. Gli utenti creano istanze della classe consumer come parte di una sottoscrizione permanente. Se il provider di eventi non è in esecuzione quando si verifica un evento, WMI avvia il provider quando è necessario recapitare gli eventi.

Nella procedura seguente viene descritto come implementare un provider di consumer di eventi.

**Per implementare un provider di consumer di eventi**

1.  Progettare le classi consumer in Managed Object Format (MOF) e registrarle con WMI. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

    I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) . Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di consumer di eventi](registering-an-event-consumer-provider.md).

2.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).

    > [!Note]  
    > I provider di consumer di eventi sono vivamente invitati a usare il modello di multithreading "both".

     

3.  Implementare l'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) per il provider.

    L'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) è l'interfaccia principale per un provider di consumer di eventi.

4.  Fornire uno o più consumer fisici per ricevere i messaggi di evento da WMI.

    Un consumer fisico è un oggetto COM che rappresenta un consumer di eventi permanenti. Tutti i consumer fisici devono implementare l'interfaccia [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Per ulteriori informazioni, vedere [implementazione di un consumer fisico](implementing-a-physical-consumer.md).

 

 




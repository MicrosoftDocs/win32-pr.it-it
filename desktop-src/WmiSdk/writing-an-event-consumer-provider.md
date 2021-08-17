---
description: Un provider di consumer di eventi è un componente dell'architettura consumer permanente che determina quale consumer di eventi permanente gestisce un determinato evento.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Scrittura di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312e0c2ecbf02d8bb0a8f491339d191aadde41a66cd3e3228c3187d5dcf689e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553098"
---
# <a name="writing-an-event-consumer-provider"></a>Scrittura di un provider di consumer di eventi

Un provider di consumer di eventi è un componente dell'architettura consumer permanente che determina quale consumer di eventi permanente gestisce un determinato evento. È necessario creare un provider di consumer di eventi insieme ai consumer di eventi permanenti per indirizzare correttamente gli eventi da WMI.

Un provider di consumer di eventi collega un provider di eventi a un elenco di classi consumer. Le istanze di queste classi consumer ricevono quindi eventi da tale provider. WMI identifica il provider di consumer a cui vengono recapitati gli eventi, in base all'istanza [**\_ \_ EventConsumerProviderRegistration,**](--eventconsumerproviderregistration.md) che associa l'istanza [**\_ \_ Win32Provider**](--win32provider.md) del provider di consumer a una classe consumer logica. Gli utenti creano istanze della classe consumer come parte di una sottoscrizione permanente. Se il provider di eventi non è in esecuzione quando si verifica un evento, WMI avvia il provider quando deve recapitare gli eventi.

La procedura seguente descrive come implementare un provider di consumer di eventi.

**Per implementare un provider di consumer di eventi**

1.  Progettare classi consumer in Managed Object Format (MOF) e registrarle con WMI. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

    I provider di classi si registrano con WMI creando [**\_ \_ un'istanza win32Provider**](--win32provider.md) e una [**\_ \_ classe EventConsumerProviderRegistration.**](--eventconsumerproviderregistration.md) Per altre informazioni, vedere [Registrazione di un provider di consumer di eventi](registering-an-event-consumer-provider.md).

2.  Implementare [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Per altre informazioni, vedere [Inizializzazione di un provider](initializing-a-provider.md).

    > [!Note]  
    > I provider di consumer di eventi sono fortemente invitati a usare il modello di multithreading "Both".

     

3.  Implementare [**l'interfaccia IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) per il provider.

    [**L'interfaccia IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) è l'interfaccia principale per un provider di consumer di eventi.

4.  Fornire uno o più consumer fisici per ricevere i messaggi di evento da WMI.

    Un consumer fisico è un oggetto COM che rappresenta un consumer di eventi permanente. Tutti i consumer fisici devono implementare [**l'interfaccia IWbemUnboundObjectSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) Per altre informazioni, vedere [Implementazione di un consumer fisico.](implementing-a-physical-consumer.md)

 

 




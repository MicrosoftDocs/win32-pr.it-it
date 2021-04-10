---
title: Implementazione del modello di sicurezza Teredo
description: Il modello di sicurezza Teredo è basato sulla tecnologia Windows Filtering Platform (WFP) incorporata in Windows Vista. Di conseguenza, si consiglia ai firewall di terze parti di utilizzare WFP per applicare il modello di sicurezza Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729050"
---
# <a name="implementing-the-teredo-security-model"></a>Implementazione del modello di sicurezza Teredo

Il modello di sicurezza Teredo è basato sulla tecnologia [Windows Filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) incorporata in Windows Vista. Di conseguenza, si consiglia ai firewall di terze parti di utilizzare WFP per applicare il modello di sicurezza [Teredo](about-teredo.md) .

Per l'implementazione generale del [modello di sicurezza Teredo](the-teredo-security-model.md) sono necessari gli elementi seguenti:

-   Un firewall host che supporta IPv6 deve essere registrato con il Centro sicurezza PC Windows (WSC) nel computer. In assenza di un firewall basato su host o di WSC, l'interfaccia Teredo non sarà disponibile per l'utilizzo. Questo è l'unico requisito per ricevere traffico richiesto da Internet tramite l'interfaccia Teredo.
-   Tutte le applicazioni che ricevono traffico non richiesto da Internet tramite l'interfaccia Teredo devono registrarsi con un firewall che supporta IPv6, ad esempio [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page), prima di ricevere il traffico non richiesto.

Un indirizzo Teredo diventerà inattivo se il traffico non è stato inviato o ricevuto sull'interfaccia Teredo per un'ora e se le applicazioni che soddisfano i criteri di sicurezza richiesti per il traffico non richiesto non sono in esecuzione o non hanno socket in ascolto aperti.

Dopo il riavvio di un computer o se l'indirizzo Teredo perde le proprie qualifiche, Windows Vista qualifica automaticamente l'indirizzo e lo rende disponibile per l'utilizzo non appena un'applicazione viene associata a socket compatibili con IPv6. È importante notare che l'opzione Windows Firewall "attraversamento bordi" impostata da un'applicazione per consentire il traffico non richiesto tramite Teredo è persistente tra i riavvii.

## <a name="firewall-requirements-for-teredo"></a>Requisiti del firewall per Teredo

I fornitori di firewall possono incorporare facilmente il supporto Teredo nei propri prodotti e proteggere gli utenti utilizzando le funzionalità della piattaforma filtro Windows. Questa operazione può essere eseguita registrando il firewall in grado di supportare IPv6 con il Centro sicurezza Windows, aggiungendo le regole appropriate nel sottolivello Teredo di WFP e usando le API predefinite in Windows per enumerare le applicazioni che potrebbero ascoltare il traffico non richiesto su Teredo. Nelle situazioni in cui non è necessario che un'applicazione ascolti il traffico richiesto su Teredo, i firewall non necessitano di regole aggiuntive aggiunte al Pam. Tuttavia, una registrazione del firewall in grado di supportare IPv6 con il Centro sicurezza Windows è ancora un requisito per rendere disponibile l'indirizzo Teredo per l'utilizzo.

Per supportare questo scenario, il firewall deve essere in grado di supportare IPv6 e registrato con il Centro sicurezza Windows. Inoltre, il firewall non deve modificare lo stato in esecuzione o di avvio del servizio Centro sicurezza PC Windows (wscsvc), in quanto Teredo dipende dalle informazioni sullo stato fornite tramite le API WSC.

L'API utilizzata per registrare un firewall con WSC può essere ottenuta contattando Microsoft all'indirizzo wscisv@microsoft.com . Un contratto di non divulgazione (NDA) è necessario per la divulgazione di questa API a causa di problemi di sicurezza.

Nella documentazione riportata di seguito vengono illustrati i filtri e le eccezioni utilizzati per garantire la compatibilità ottimale con Teredo:

-   [Implementazione di filtri firewall per Teredo](implementing-firewall-filters-for-teredo.md)
-   [Eccezioni del firewall richieste per Teredo](required-firewall-exceptions-for-teredo.md)
-   [Eccezioni della piattaforma filtro Windows richieste per Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisiti del firewall per altre tecnologie di transizione IPv6

Per supportare altre tecnologie di transizione IPv6 (ad esempio 6to4 e ISATAP), il prodotto firewall host deve essere in grado di elaborare il traffico IPv6. Il protocollo IP 41 indica quando un'intestazione IPv6 segue un'intestazione IPv4. Quando un firewall host rileva il protocollo 41, deve riconoscere che il pacchetto è un pacchetto incapsulato in IPv6 e, di conseguenza, deve elaborare il pacchetto in modo appropriato e prendere le decisioni di accettazione/negazione in base alle regole IPv6 nei criteri.

 

 
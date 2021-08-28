---
title: Implementazione del modello Teredo security
description: Il Teredo di sicurezza è basato sulla tecnologia Windows Filtering Platform (WFP) integrata in Windows Vista. Di conseguenza, è consigliabile che i firewall di terze parti usino wfp per applicare il Teredo di sicurezza.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cad78b7c1512e0f1c632ecd27d0bb9580ac3796d6d36001a1cd19fb72c7b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001749"
---
# <a name="implementing-the-teredo-security-model"></a>Implementazione del modello Teredo security

Il Teredo di sicurezza basato sulla tecnologia [Windows Filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) integrata in Windows Vista. Di conseguenza, è consigliabile che i firewall di terze parti usino wfp per applicare il [Teredo](about-teredo.md) di sicurezza.

L'implementazione generale del [Teredo di sicurezza richiede](the-teredo-security-model.md) quanto segue:

-   Un firewall host con supporto IPv6 deve essere registrato con Sicurezza di Windows Center (WSC) nel computer. In assenza di un firewall basato su host o di WSC, l'interfaccia Teredo non sarà disponibile per l'uso. Questo è l'unico requisito per ricevere il traffico richiesto da Internet tramite l Teredo intervazione.
-   Qualsiasi applicazione che riceve traffico non richiesto da Internet tramite l'interfaccia Teredo deve registrarsi con un firewall con supporto IPv6, ad esempio [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page), prima di ricevere il traffico non richiesto.

Un indirizzo Teredo diventa inattivo se il traffico non è stato inviato o ricevuto sull'interfaccia Teredo per un'ora e se le applicazioni che soddisfano i criteri di sicurezza richiesti per il traffico non richiesto non sono in esecuzione o non hanno socket di ascolto aperti.

Dopo il riavvio di un computer o se l'indirizzo Teredo perde le proprie qualifiche, Windows Vista qualifica automaticamente l'indirizzo e lo rende disponibile per l'uso non appena un'applicazione si associa ai socket con supporto IPv6. È importante notare che l'opzione Windows Firewall "Edge Traversal" impostata da un'applicazione per consentire il traffico non richiesto tramite Teredo è persistente tra i riavvii.

## <a name="firewall-requirements-for-teredo"></a>Requisiti del firewall per Teredo

I fornitori di firewall possono incorporare Teredo supporto nei propri prodotti e proteggere gli utenti usando le funzionalità di Windows Filtering Platform. Questa operazione può essere eseguita registrando il firewall con supporto per IPv6 con il centro Sicurezza di Windows, aggiungendo regole appropriate nel sottolivelli Teredo wfp e usando le API predefinite in Windows per enumerare le applicazioni che potrebbero restare in ascolto del traffico non richiesto su Teredo. Nei casi in cui un'applicazione non deve restare in ascolto del traffico richiesto Teredo, i firewall non richiedono regole aggiuntive aggiunte al WFP. Tuttavia, una registrazione del firewall con supporto IPv6 con Sicurezza di Windows Center è ancora un requisito per rendere disponibile l'indirizzo Teredo per l'uso.

Per supportare questo scenario, il firewall deve essere con supporto per IPv6 e registrato con Sicurezza di Windows Center. Inoltre, il firewall non deve modificare lo stato di esecuzione o avvio del servizio Sicurezza di Windows Center (wscsvc), perché Teredo dipende dalle informazioni sullo stato fornite tramite le API WSC.

L'API utilizzata per registrare un firewall con WSC può essere ottenuta contattando Microsoft all'indirizzo wscisv@microsoft.com . Per la divulgazione di questa API è necessario un contratto di non divulgazione (NDA) a causa di problemi di sicurezza.

La documentazione seguente dettaglia i filtri e le eccezioni utilizzati per garantire la compatibilità ottimale con Teredo:

-   [Implementazione di filtri firewall per Teredo](implementing-firewall-filters-for-teredo.md)
-   [Eccezioni del firewall necessarie per Teredo](required-firewall-exceptions-for-teredo.md)
-   [Richieste Windows eccezioni della piattaforma di filtro per Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Requisiti del firewall per altre tecnologie di transizione IPv6

Per supportare altre tecnologie di transizione IPv6 (ad esempio 6to4 e ISATAP), il prodotto firewall host deve essere in grado di elaborare il traffico IPv6. Il protocollo IP 41 indica quando un'intestazione IPv6 segue un'intestazione IPv4. Quando un firewall host rileva il protocollo 41, deve riconoscere che il pacchetto è un pacchetto incapsulato IPv6 e di conseguenza deve elaborare il pacchetto in modo appropriato e prendere le decisioni di accettazione/rifiuto in base alle regole IPv6 nei criteri.

 

 
---
title: Architettura e interoperabilità
description: Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e l'automazione dell'interfaccia utente Microsoft e i componenti che consentono l'interoperabilità tra applicazioni basate su due tecnologie diverse.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104117295"
---
# <a name="architecture-and-interoperability"></a>Architettura e interoperabilità

Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e l'automazione dell'interfaccia utente Microsoft e i componenti che consentono l'interoperabilità tra applicazioni basate su due tecnologie diverse.

Per ulteriori informazioni sull'interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente, vedere [infrastruttura comune](common-infrastructure.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Architettura di Microsoft Active Accessibility](#microsoft-active-accessibility-architecture)
-   [Architettura di automazione interfaccia utente](#ui-automation-architecture)
-   [Interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Interfaccia IAccessibleEx](#the-iaccessibleex-interface)
-   [Argomenti correlati](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Architettura di Microsoft Active Accessibility

Microsoft Active Accessibility espone informazioni di base sui controlli, ad esempio il nome del controllo, la posizione sullo schermo e il tipo di controllo, nonché informazioni sullo stato, ad esempio la visibilità e lo stato di abilitazione/disabilitazione. L'interfaccia utente è rappresentata come una gerarchia di oggetti accessibili; le modifiche e le azioni sono rappresentate come WinEvents.

Microsoft Active Accessibility è costituito dai componenti seguenti:

-   Oggetto accessibile: elemento dell'interfaccia utente logico, ad esempio un pulsante, rappresentato da un'interfaccia di Component Object Model [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (com) e da un identificatore figlio Integer (childID).
-   WinEvents: un sistema di eventi che consente ai server di notificare ai client quando un oggetto accessibile viene modificato. Per ulteriori informazioni, vedere [winEvents](winevents-infrastructure.md).
-   OLEACC.dll: la libreria a collegamento dinamico in fase di esecuzione che fornisce l'API Microsoft Active Accessibility e il Framework di sistema di accessibilità. OLEACC implementa oggetti proxy che forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard, inclusi i controlli utente, i menu utente e i controlli comuni.

Per Microsoft Active Accessibility, il componente di sistema di OLEACC (Accessibility Framework) consente la comunicazione tra le tecnologie per l'accesso facilitato (strumenti di accessibilità) e le applicazioni, come illustrato nella figura seguente.

![illustrazione che Mostra come gli strumenti di accessibilità interagiscono con le applicazioni](images/msaaarch.gif)

Le applicazioni (server Microsoft Active Accessibility) forniscono informazioni di accessibilità dell'interfaccia utente agli strumenti (Microsoft Active Accessibility client), che interagiscono con l'interfaccia utente per conto degli utenti. Il limite del codice è un limite programmatico e un processo.

## <a name="ui-automation-architecture"></a>Architettura di automazione interfaccia utente

Con l'automazione dell'interfaccia utente, il componente principale di automazione interfaccia utente (UIAutomationCore.dll) viene caricato sia nei processi degli strumenti di accessibilità che nelle applicazioni. Il componente di base gestisce la comunicazione tra processi, fornisce servizi di livello superiore, ad esempio la ricerca di elementi in base ai valori delle proprietà, e consente il recupero o la memorizzazione nella cache delle proprietà, che offre prestazioni migliori rispetto all'implementazione di Microsoft Active Accessibility.

Automazione interfaccia utente include oggetti proxy che forniscono informazioni sull'interfaccia utente sugli elementi standard dell'interfaccia utente, ad esempio controlli utente, menu utente e controlli comuni. Include anche proxy che consentono ai client di automazione interfaccia utente di ottenere informazioni sull'interfaccia utente da Microsoft Active Accessibility server.

Nella figura seguente sono illustrate le relazioni tra i diversi Compontents di automazione interfaccia utente utilizzati negli strumenti di accessibilità (client) e nelle applicazioni (provider).

![illustrazione che Mostra come i componenti degli strumenti di accessibilità interagiscono con quelli delle applicazioni](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente

L'automazione interfaccia utente di Microsoft Active Accessibility Bridge consente ai client Microsoft Active Accessibility di accedere ai provider di automazione interfaccia utente convertendo il modello a oggetti di automazione interfaccia utente in un modello a oggetti di Microsoft Active Accessibility. La figura seguente mostra il ruolo del Bridge di automazione interfaccia utente-a-Microsoft Active Accessibility.

![illustrazione che illustra il funzionamento dell'automazione interfaccia utente con gli strumenti e le applicazioni di accessibilità](images/uiatomsaabridge.gif)

Analogamente, il proxy di automazione da Active Accessibility a interfaccia utente Microsoft converte i modelli a oggetti server basati su Microsoft Active Accessibility per i client di automazione interfaccia utente. La figura seguente mostra il ruolo del proxy di automazione da Active Accessibility a interfaccia utente Microsoft.

![illustrazione che illustra il funzionamento del proxy di automazione interfaccia utente con strumenti e applicazioni per l'accessibilità](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>Interfaccia IAccessibleEx

L'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) consente alle applicazioni esistenti o alle librerie dell'interfaccia utente di estendere il modello a oggetti di Microsoft Active Accessibility per supportare l'automazione dell'interfaccia utente senza riscrivere l'implementazione da zero. Con **IAccessibleEx** è possibile implementare solo le proprietà aggiuntive di automazione interfaccia utente e i pattern di controllo necessari per descrivere completamente l'interfaccia utente e le relative funzionalità.

Poiché il proxy di automazione da Active Accessibility a interfaccia utente di Microsoft converte i modelli a oggetti di Microsoft Active Accessibility server abilitati per [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)come modelli a oggetti di automazione interfaccia utente, i client di automazione interfaccia utente non devono eseguire operazioni aggiuntive. L'interfaccia **IAccessibleEx** può inoltre consentire ai client Microsoft Active Accessibility in-process di interagire direttamente con i provider di automazione interfaccia utente.

Per ulteriori informazioni, vedere [l'interfaccia IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'API di automazione di Windows](windows-automation-api-overview.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato](uiauto-securityoverview.md)
</dt> </dl>

 

 





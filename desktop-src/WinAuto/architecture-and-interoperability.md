---
title: Architettura e interoperabilità
description: Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e Microsoft Automazione interfaccia utente e i componenti che consentono l'interoperabilità tra applicazioni basate sulle due tecnologie diverse.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b146fa2d628ff64d2dcf714a1f860bee28c2f0f816e057f6b411e8344462fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053019"
---
# <a name="architecture-and-interoperability"></a>Architettura e interoperabilità

Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e Microsoft Automazione interfaccia utente e i componenti che consentono l'interoperabilità tra applicazioni basate sulle due tecnologie diverse.

Per altre informazioni sull'interoperabilità Microsoft Active Accessibility e Automazione interfaccia utente, vedere [Infrastruttura comune](common-infrastructure.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Microsoft Active Accessibility architettura](#microsoft-active-accessibility-architecture)
-   [Automazione interfaccia utente architettura](#ui-automation-architecture)
-   [Microsoft Active Accessibility e Automazione interfaccia utente interoperabilità](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Interfaccia IAccessibleEx](#the-iaccessibleex-interface)
-   [Argomenti correlati](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Microsoft Active Accessibility architettura

Microsoft Active Accessibility informazioni di base sui controlli, ad esempio il nome del controllo, la posizione sullo schermo e il tipo di controllo, nonché informazioni sullo stato, ad esempio visibilità e stato abilitato/disabilitato. L'interfaccia utente è rappresentata come una gerarchia di oggetti accessibili. le modifiche e le azioni sono rappresentate come Eventi WinEvent.

Microsoft Active Accessibility è costituito dai componenti seguenti:

-   Oggetto accessibile: elemento logico dell'interfaccia utente (ad esempio un pulsante) rappresentato da [**un'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) e da un identificatore figlio integer (ChildID).
-   WinEvents: sistema di eventi che consente ai server di inviare notifiche ai client quando viene modificato un oggetto accessibile. Per altre informazioni, vedere [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll: libreria di runtime a collegamento dinamico che fornisce l'API Microsoft Active Accessibility e il framework del sistema di accessibilità. OLEACC implementa oggetti proxy che forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard, inclusi i controlli USER, i menu USER e i controlli comuni.

Ad Microsoft Active Accessibility, il componente di sistema del framework di accessibilità (OLEACC) consente la comunicazione tra le tecnologie di accessibilità (strumenti di accessibilità) e le applicazioni, come illustrato nella figura seguente.

![Figura che illustra l'interazione degli strumenti di accessibilità con le applicazioni](images/msaaarch.gif)

Le applicazioni (Microsoft Active Accessibility server) forniscono informazioni sull'accessibilità dell'interfaccia utente agli strumenti (Microsoft Active Accessibility client), che interagiscono con l'interfaccia utente per conto degli utenti. Il limite del codice è sia un limite a livello di codice che un limite di processo.

## <a name="ui-automation-architecture"></a>Automazione interfaccia utente architettura

Con Automazione interfaccia utente, il Automazione interfaccia utente core (UIAutomationCore.dll) viene caricato nei processi degli strumenti di accessibilità e delle applicazioni. Il componente di base gestisce la comunicazione tra processi, fornisce servizi di livello superiore, ad esempio la ricerca di elementi in base ai valori delle proprietà e consente il recupero bulk o la memorizzazione nella cache delle proprietà, che offre prestazioni migliori rispetto all'implementazione Microsoft Active Accessibility.

Automazione interfaccia utente oggetti proxy che forniscono informazioni sull'interfaccia utente sugli elementi dell'interfaccia utente standard, ad esempio controlli UTENTE, menu UTENTE e controlli comuni. Include anche proxy che consentono ai client Automazione interfaccia utente di ottenere informazioni sull'interfaccia utente Microsoft Active Accessibility server.

La figura seguente illustra le relazioni tra i vari Automazione interfaccia utente usati negli strumenti di accessibilità (client) e nelle applicazioni (provider).

![Illustrazione che illustra l'interazione dei componenti degli strumenti di accessibilità con quelli delle applicazioni](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Microsoft Active Accessibility e Automazione interfaccia utente interoperabilità

L'Automazione interfaccia utente a Microsoft Active Accessibility Bridge consente ai client Microsoft Active Accessibility di accedere ai provider Automazione interfaccia utente convertendo il modello a oggetti Automazione interfaccia utente in un modello a oggetti Microsoft Active Accessibility dati. La figura seguente mostra il ruolo dell'Automazione interfaccia utente da Microsoft Active Accessibility Bridge.

![Figura che illustra il funzionamento dell'automazione interfaccia utente con gli strumenti e le applicazioni di accessibilità](images/uiatomsaabridge.gif)

Analogamente, il proxy Microsoft Active Accessibility-to-Automazione interfaccia utente converte i modelli Microsoft Active Accessibility a oggetti server basati su Automazione interfaccia utente client. Nella figura seguente viene illustrato il ruolo del Microsoft Active Accessibility da Automazione interfaccia utente proxy.

![Illustrazione che illustra il funzionamento del proxy di automazione interfaccia utente con gli strumenti e le applicazioni di accessibilità](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>Interfaccia IAccessibleEx

[**L'interfaccia IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) consente alle applicazioni o alle librerie dell'interfaccia utente esistenti di estendere il modello Microsoft Active Accessibility a oggetti per supportare Automazione interfaccia utente senza riscrivere l'implementazione da zero. Con **IAccessibleEx** è possibile implementare solo le proprietà Automazione interfaccia utente aggiuntive e i pattern di controllo necessari per descrivere completamente l'interfaccia utente e le relative funzionalità.

Poiché Microsoft Active Accessibility-to-Automazione interfaccia utente Proxy converte i modelli a oggetti dei server Microsoft Active Accessibility abilitati per [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)come modelli Automazione interfaccia utente Automazione interfaccia utente, i client Automazione interfaccia utente non devono eseguire operazioni aggiuntive. **L'interfaccia IAccessibleEx** può anche consentire ai client Microsoft Active Accessibility in-process di interagire direttamente con Automazione interfaccia utente provider.

Per altre informazioni, vedere [Interfaccia IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Panoramica dell'API di automazione](windows-automation-api-overview.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Considerazioni sulla sicurezza per assistive Technologies](uiauto-securityoverview.md)
</dt> </dl>

 

 





---
title: Panoramica tecnica
description: Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono agli utenti con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni eseguite in Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712946"
---
# <a name="technical-overview"></a>Panoramica tecnica

Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono agli utenti con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni eseguite in Microsoft Windows.

Microsoft Active Accessibility si basa sul Component Object Model (COM), sviluppato da Microsoft ed è uno standard di settore che definisce un modo comune per la comunicazione tra le applicazioni e i sistemi operativi. Microsoft Active Accessibility è costituito dai componenti seguenti:

-   Interfaccia COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), che espone informazioni sugli elementi dell'interfaccia utente. **IAccessible** dispone inoltre di proprietà e metodi per ottenere informazioni e modificare tale elemento dell'interfaccia utente.
-   WinEvents, un sistema di eventi che consente ai server di notificare ai client quando un oggetto accessibile viene modificato.
-   Oleacc.dll, un supporto o una DLL di run-time.

Microsoft Active Accessibility DLL, Oleacc.dll, è costituito dai componenti seguenti:

-   Funzioni che consentono ai client di richiedere un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (ad esempio, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Funzioni che consentono ai server di restituire un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un client, ad esempio [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).
-   Funzioni per ottenere il testo localizzato per il ruolo e i codici di stato (ad esempio, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) e [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Alcune funzioni helper ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Codice che fornisce l'implementazione predefinita di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i controlli utente e COMCTL standard. Poiché queste implementano **IAccessible** per conto dei controlli di sistema, sono note come *proxy*.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Funzionamento di Active Accessibility](how-active-accessibility-works.md)
-   [Nozioni di base Active Accessibility](active-accessibility-basics.md)
-   [Linee guida sul server](server-guidelines.md)
-   [Linee guida sui client](client-guidelines.md)
-   [Linee guida per COM e Unicode](com-and-unicode-guidelines.md)

 

 





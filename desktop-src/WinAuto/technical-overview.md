---
title: Panoramica tecnica
description: Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono alle persone con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni in esecuzione in Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e2bfd984dce863a2bdcdbd41d7b3d72b521861177bc4086a93eb578eb71c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325153"
---
# <a name="technical-overview"></a>Panoramica tecnica

Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono alle persone con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni in esecuzione in Microsoft Windows.

Microsoft Active Accessibility è basato su Component Object Model (COM), sviluppato da Microsoft ed è uno standard di settore che definisce un modo comune per le applicazioni e i sistemi operativi di comunicare. Microsoft Active Accessibility è costituito dai componenti seguenti:

-   Interfaccia COM [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)che espone informazioni sugli elementi dell'interfaccia utente. **IAccessible include** anche proprietà e metodi per ottenere informazioni su tale elemento dell'interfaccia utente e modificarlo.
-   WinEvents, un sistema di eventi che consente ai server di notificare ai client quando viene modificato un oggetto accessibile.
-   Oleacc.dll, una DLL di supporto o di run-time.

La DLL Microsoft Active Accessibility, Oleacc.dll, è costituita dai componenti seguenti:

-   Funzioni che consentono ai client di richiedere un puntatore di interfaccia [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ad esempio [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   Funzioni che consentono ai server di restituire un [**puntatore di**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfaccia IAccessible a un client (ad esempio, [**LresultFromObject).**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Funzioni per ottenere il testo localizzato per i codici di ruolo e di stato (ad [**esempio, GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) e [**GetStateText).**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)
-   Alcune funzioni helper ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Codice che fornisce l'implementazione predefinita di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i controlli USER e COMCTL standard. Poiché **implementano IAccessible** per conto dei controlli di sistema, sono noti *come proxy.*

## <a name="in-this-section"></a>Contenuto della sezione

-   [Funzionamento Active Accessibility](how-active-accessibility-works.md)
-   [Active Accessibility di base](active-accessibility-basics.md)
-   [Linee guida per i server](server-guidelines.md)
-   [Linee guida per i client](client-guidelines.md)
-   [Linee guida com e Unicode](com-and-unicode-guidelines.md)

 

 





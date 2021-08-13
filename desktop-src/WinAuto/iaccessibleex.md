---
title: Interfaccia IAccessibleEx
description: I controlli che non dispongono di un provider Microsoft Automazione interfaccia utente, ma che implementano IAccessible, possono essere facilmente aggiornati per fornire alcune funzionalità di Automazione interfaccia utente implementando l'interfaccia IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170e6160a05350fa459090b2f51dbedd618ebdb81512a7e9730b50f8533ef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566012"
---
# <a name="the-iaccessibleex-interface"></a>Interfaccia IAccessibleEx

I controlli che non dispongono di un provider Microsoft Automazione interfaccia utente, ma che implementano [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)possono essere facilmente aggiornati per fornire alcune funzionalità Automazione interfaccia utente implementando [**l'interfaccia IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Questa interfaccia consente al controllo di esporre le Automazione interfaccia utente e i pattern di controllo, senza la necessità di un'implementazione completa delle interfacce del provider Automazione interfaccia utente, ad esempio [**IRawElementProviderFragment.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) Per usare **IAccessibleEx,** **IRawElementProviderFragment** e tutte le altre interfacce Automazione interfaccia utente, includere il file di intestazione UIAutomation.h nel codice sorgente.

Si consideri ad esempio un controllo personalizzato con un valore di intervallo. Il Microsoft Active Accessibility server per il controllo definisce il ruolo del controllo ed è in grado di restituire il valore corrente. Tuttavia, poiché Microsoft Active Accessibility non definisce le proprietà minima e massima, il server non dispone dei mezzi per restituire i valori minimo e massimo del controllo. Un client Automazione interfaccia utente è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà Microsoft Active Accessibility, perché il core Automazione interfaccia utente può ottenerlo tramite [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Tuttavia, senza l'accesso a un'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) nell'oggetto, Automazione interfaccia utente non è in grado di recuperare i valori massimo e minimo.

Lo sviluppatore del controllo può fornire un provider Automazione interfaccia utente completo per il controllo, ma ciò significa duplicare gran parte delle funzionalità esistenti dell'implementazione [**di IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ad esempio la navigazione e le proprietà comuni. Al contrario, lo sviluppatore può continuare a fare affidamento su **IAccessible** per fornire questa funzionalità, aggiungendo al tempo stesso il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Linee guida per l'implementazione di IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementazione di IAccessibleEx per i provider](implementing-iaccessibleex-for-providers.md)
-   [Uso di IAccessibleEx da un client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura comune](common-infrastructure.md)
</dt> </dl>

 

 





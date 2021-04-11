---
title: Interfaccia IAccessibleEx
description: I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft, ma che implementano IAccessible, possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente implementando l'interfaccia IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116885"
---
# <a name="the-iaccessibleex-interface"></a>Interfaccia IAccessibleEx

I controlli che non dispongono di un provider di automazione interfaccia utente Microsoft, ma che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), possono essere facilmente aggiornati per fornire alcune funzionalità di automazione interfaccia utente implementando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Questa interfaccia consente al controllo di esporre le proprietà e i pattern di controllo di automazione interfaccia utente senza la necessità di un'implementazione completa delle interfacce del provider di automazione interfaccia utente, ad esempio [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Per usare **IAccessibleEx**, **IRawElementProviderFragment** e tutte le altre interfacce di automazione interfaccia utente, includere il file di intestazione UIAutomation. h nel codice sorgente.

Si consideri, ad esempio, un controllo personalizzato con un valore di intervallo. Il server Microsoft Active Accessibility per il controllo definisce il ruolo del controllo ed è in grado di restituire il valore corrente. Tuttavia, poiché Microsoft Active Accessibility non definisce le proprietà minime e massime, il server non dispone dei mezzi per restituire i valori minimo e massimo del controllo. Un client di automazione interfaccia utente è in grado di recuperare il ruolo del controllo, il valore corrente e altre proprietà di Active Accessibility Microsoft, perché il nucleo di automazione interfaccia utente può ottenere tali proprietà tramite [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Tuttavia, senza l'accesso a un'interfaccia [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sull'oggetto, l'automazione dell'interfaccia utente non è in grado di recuperare i valori massimi e minimi.

Lo sviluppatore del controllo può fornire un provider di automazione interfaccia utente completo per il controllo, ma ciò comporta la duplicazione di gran parte delle funzionalità esistenti dell'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ad esempio la navigazione e le proprietà comuni. Lo sviluppatore può invece continuare a basarsi su **IAccessible** per fornire questa funzionalità, aggiungendo il supporto per le proprietà specifiche del controllo tramite [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>Contenuto della sezione

-   [Linee guida per l'implementazione di IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementazione di IAccessibleEx per i provider](implementing-iaccessibleex-for-providers.md)
-   [Uso di IAccessibleEx da un client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura comune](common-infrastructure.md)
</dt> </dl>

 

 





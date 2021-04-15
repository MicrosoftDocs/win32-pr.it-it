---
title: Proprietà Description (funzionalità di accessibilità di Windows)
description: La proprietà Description di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474980"
---
# <a name="description-property-windows-accessibility-features"></a>Proprietà Description (funzionalità di accessibilità di Windows)

> [!Note]  
> La proprietà **Description** viene spesso usata in modo non corretto e non è supportata dall'automazione interfaccia utente Microsoft. Gli sviluppatori di Microsoft Active Accessibility server non devono utilizzare questa proprietà. Se sono necessarie altre informazioni per gli scenari di accessibilità e automazione, usare le proprietà supportate dagli elementi di automazione interfaccia utente e dai pattern di controllo.

 

La proprietà **Description** di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto. La descrizione viene utilizzata principalmente per fornire un contesto più ampio per utenti ipovedenti o ipovedenti, ma viene anche utilizzata per la ricerca del contesto o altre applicazioni. Questa proprietà può aiutare gli utenti a comprendere un'icona o l'aspetto visivo generale.

La proprietà **Description** viene recuperata chiamando [**IAccessible:: Get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Quando supportare la proprietà Description

I server supportano la proprietà **Description** se la descrizione non è ovvia o se non è ridondante in base alle proprietà [**Name**](name-property.md), [**Role**](role-property.md), [**state**](state-property.md)e [**value**](value-property.md) dell'oggetto. Ad esempio, un pulsante con etichetta "OK" non richiede informazioni aggiuntive, mentre un pulsante che mostra un'immagine di un cactus. Il **nome**, il **ruolo** e le proprietà della [**Guida**](help-property.md) per un pulsante di questo tipo ne descrivono lo scopo, ma la proprietà **Description** trasmette informazioni meno tangibili; ad esempio, "questo pulsante Mostra un'immagine di un cactus".

Un server Microsoft Active Accessibility può aggiungere il supporto per l'automazione dell'interfaccia utente usando un' [annotazione diretta](direct-annotation.md), usando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o implementando Microsoft Active Accessibility e l'automazione dell'interfaccia utente side-by-side con entrambe le implementazioni che gestiscono il messaggio [**WM \_ GetObject**](wm-getobject.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'annotazione diretta](using-direct-annotation.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 





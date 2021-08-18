---
title: Proprietà Description (Windows accessibilità)
description: La proprietà Description di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994231"
---
# <a name="description-property-windows-accessibility-features"></a>Proprietà Description (Windows accessibilità)

> [!Note]  
> La **proprietà Description** viene spesso usata in modo non corretto e non è supportata da Microsoft Automazione interfaccia utente. Microsoft Active Accessibility gli sviluppatori di server non devono usare questa proprietà. Se sono necessarie altre informazioni per gli scenari di accessibilità e automazione, usare le proprietà supportate Automazione interfaccia utente elementi e pattern di controllo.

 

La proprietà **Description** di un oggetto fornisce una descrizione testuale dell'aspetto visivo di un oggetto. La descrizione viene usata principalmente per fornire un contesto più ampio per utenti non vedenti o non vedenti, ma viene usata anche per la ricerca di contesto o altre applicazioni. Questa proprietà consente agli utenti di comprendere un'icona o l'aspetto visivo complessivo.

La **proprietà Description** viene recuperata chiamando [**IAccessible::get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Quando supportare la proprietà Description

I server supportano la proprietà **Description** se la descrizione non è ovvia o quando non è ridondante in base alle proprietà [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md)e [**Value dell'oggetto.**](value-property.md) Ad esempio, un pulsante con etichetta "OK" non avrebbe bisogno di informazioni aggiuntive, mentre un pulsante che mostra un'immagine di un cactus. Le **proprietà Name,** **Role** e [**Help**](help-property.md) per un pulsante di questo tipo ne descrivono lo scopo, ma la **proprietà Description** fornisce informazioni meno tangibili. ad esempio "Questo pulsante mostra un'immagine di un cactus".

Un server Microsoft Active Accessibility può aggiungere il supporto per [](direct-annotation.md)Automazione interfaccia utente usando l'annotazione diretta , usando l'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o implementando Microsoft Active Accessibility e Automazione interfaccia utente side-by-side con entrambe le implementazioni che gestisce il messaggio [**WM \_ GETOBJECT.**](wm-getobject.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'annotazione diretta](using-direct-annotation.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 





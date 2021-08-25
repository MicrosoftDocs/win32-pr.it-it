---
title: Creazione dell'oggetto CUIAutomation
description: Questa sezione descrive come iniziare a scrivere un'applicazione client Microsoft Automazione interfaccia utente creando un'istanza di un oggetto che implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- client, creazione dell'oggetto CUIAutomation
- clients,CUIAutomation object
- Automazione interfaccia utente,CUIAutomation object
- Automazione interfaccia utente,creazione dell'oggetto CUIAutomation
- creazione di un oggetto CUIAutomation
- Oggetto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b9720ce31f883c4561ae3f82372d902a0dcc3fbfca4bae6de998ce438a6d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795491"
---
# <a name="creating-the-cuiautomation-object"></a>Creazione dell'oggetto CUIAutomation

Questa sezione descrive come iniziare a scrivere un'applicazione client Microsoft Automazione interfaccia utente creando un'istanza di un oggetto che implementa [**IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)

In questo argomento sono contenute le sezioni seguenti.

-   [Oggetto CUIAutomation](#the-cuiautomation-object)
-   [Creazione dell'oggetto](#creating-the-object)
-   [Argomenti correlati](#related-topics)

## <a name="the-cuiautomation-object"></a>Oggetto CUIAutomation

Il primo passaggio dell'Automazione interfaccia utente consiste nel creare un oggetto della [**classe CUIAutomation.**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) Questo oggetto espone [**l'interfaccia IUIAutomation,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) ovvero il gateway per tutti gli altri oggetti e interfacce usati dalle applicazioni client. Tra le altre cose, **IUIAutomation** viene usato per le attività seguenti:

-   Sottoscrizione di eventi.
-   Creazione di condizioni. Le condizioni sono oggetti usati per restringere l'ambito delle ricerche Automazione interfaccia utente elementi.
-   Recupero Automazione interfaccia utente elementi direttamente dal desktop (l'elemento radice) o dalle coordinate dello schermo o dagli handle di finestra.
-   Creazione di oggetti albero albero che possono essere utilizzati per esplorare la gerarchia di Automazione interfaccia utente elementi.
-   Conversione di tipi di dati.

## <a name="creating-the-object"></a>Creazione dell'oggetto

Per iniziare a usare Automazione interfaccia utente nell'applicazione, seguire questa procedura:

-   Includere UIAutomation.h nelle intestazioni del progetto. UIAutomation.h introduce le altre intestazioni che definiscono l'API.
-   Dichiarare un puntatore a [**IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)
-   Inizializzare Component Object Model (COM).
-   Creare un'istanza di [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recuperare [**l'interfaccia IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore.

La funzione di esempio seguente inizializza COM e quindi crea l'oggetto [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) recuperando [**l'interfaccia IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore *ppAutomation.*


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Ottenere elementi di automazione interfaccia utente](uiauto-obtainingelements.md)
</dt> </dl>

 

 
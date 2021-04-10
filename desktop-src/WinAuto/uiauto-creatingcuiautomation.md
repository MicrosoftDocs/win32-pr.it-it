---
title: Creazione dell'oggetto CUIAutomation
description: Questa sezione descrive come iniziare a scrivere un'applicazione client di automazione interfaccia utente Microsoft creando un'istanza di un oggetto che implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- client, creazione oggetto CUIAutomation
- client, oggetto CUIAutomation
- Automazione interfaccia utente, oggetto CUIAutomation
- Automazione interfaccia utente, creazione oggetto CUIAutomation
- creazione dell'oggetto CUIAutomation
- Oggetto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963141"
---
# <a name="creating-the-cuiautomation-object"></a>Creazione dell'oggetto CUIAutomation

Questa sezione descrive come iniziare a scrivere un'applicazione client di automazione interfaccia utente Microsoft creando un'istanza di un oggetto che implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

In questo argomento sono contenute le sezioni seguenti.

-   [Oggetto CUIAutomation](#the-cuiautomation-object)
-   [Creazione dell'oggetto](#creating-the-object)
-   [Argomenti correlati](#related-topics)

## <a name="the-cuiautomation-object"></a>Oggetto CUIAutomation

Il primo passaggio nell'uso di automazione interfaccia utente consiste nel creare un oggetto della classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) . Questo oggetto espone l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , che rappresenta il gateway per tutti gli altri oggetti e le interfacce utilizzati dalle applicazioni client. Tra le altre cose, **IUIAutomation** viene usato per le attività seguenti:

-   Sottoscrizione degli eventi.
-   Creazione di condizioni. Le condizioni sono oggetti utilizzati per limitare l'ambito delle ricerche degli elementi di automazione interfaccia utente.
-   Ottenere gli elementi di automazione interfaccia utente direttamente dal desktop (elemento radice) o dalle coordinate dello schermo o dagli handle di finestra.
-   Creazione di oggetti Walker di albero che possono essere usati per spostarsi nella gerarchia degli elementi di automazione interfaccia utente.
-   Conversione di tipi di dati.

## <a name="creating-the-object"></a>Creazione dell'oggetto

Per iniziare a usare automazione interfaccia utente nell'applicazione, seguire questa procedura:

-   Includere UIAutomation. h nelle intestazioni del progetto. UIAutomation. h riporta le altre intestazioni che definiscono l'API.
-   Dichiarare un puntatore a [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Inizializzare il Component Object Model (COM).
-   Creare un'istanza di [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recuperare l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore.

La funzione di esempio seguente inizializza COM e quindi crea l'oggetto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , recuperando l'interfaccia [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) nel puntatore *ppAutomation* .


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

 

 
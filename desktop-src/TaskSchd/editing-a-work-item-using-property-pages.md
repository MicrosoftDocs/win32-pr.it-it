---
title: Modifica di un elemento di lavoro tramite le pagine delle proprietà
description: È possibile modificare le proprietà di un elemento di lavoro usando l'interfaccia utente grafica fornita da Utilità di pianificazione Service.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- modifica di elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100431"
---
# <a name="editing-a-work-item-using-property-pages"></a>Modifica di un elemento di lavoro tramite le pagine delle proprietà

È possibile modificare le proprietà di un elemento di lavoro usando l'interfaccia utente grafica fornita da Utilità di pianificazione Service. Attualmente, gli unici elementi di lavoro validi sono le attività.

La procedura seguente descrive come modificare un'attività usando le relative pagine delle proprietà.

**Per modificare un'attività usando le relative pagine delle proprietà**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questi esempi presuppongono che il Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.
3.  Chiamare [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) per visualizzare le pagine delle proprietà per l'attività.
4.  Modificare le proprietà dell'attività in base alle esigenze, quindi fare clic su OK per accettare i nuovi valori e rimuovere le pagine delle proprietà visualizzate.



| Per un esempio di codice di                                                                                      | Vedere                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Visualizzazione delle pagine delle proprietà per un'attività nota e consentire a un utente di modificare le proprietà dell'elemento di lavoro | [Esempio di codice C/C++: modifica di un elemento di lavoro](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
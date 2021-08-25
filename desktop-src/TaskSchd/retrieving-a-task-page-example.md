---
title: Esempio di recupero di una pagina attività
description: Per recuperare una pagina di attività, è necessario chiamare ITask QueryInterface per recuperare l'interfaccia IProvideTaskPage, quindi chiamare IProvideTaskPage GetPage. Il metodo GetPage restituisce un handle alla pagina, che può quindi essere usato per visualizzare la pagina richiesta.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recupero di pagine attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d619f76b4de416fe2bef9faa679851c613df05e427d6203a6a91936644ad07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872271"
---
# <a name="retrieving-a-task-page-example"></a>Esempio di recupero di una pagina attività

Per recuperare una pagina di attività, è necessario chiamare **ITask::QueryInterface** per recuperare [**l'interfaccia IProvideTaskPage,**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) quindi chiamare [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). Il **metodo GetPage** restituisce un handle alla pagina, che può quindi essere usato per visualizzare la pagina richiesta.

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate quando non sono più necessarie.

 

Nella procedura seguente viene descritto come creare un nuovo trigger.

**Per creare un nuovo trigger**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare **ITask::QueryInterface** per recuperare [**l'interfaccia IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) per recuperare la pagina.
4.  Usando l'handle di pagina restituito, visualizzare la pagina.



| Per un esempio di codice di                                   | Vedere                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recupero e visualizzazione della pagina Attività di un'attività nota | [Recupero di una pagina attività](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
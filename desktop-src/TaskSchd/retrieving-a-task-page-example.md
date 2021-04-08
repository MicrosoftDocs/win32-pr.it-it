---
title: Esempio di recupero di una pagina attività
description: Per recuperare una pagina di attività, è necessario chiamare ITask QueryInterface per recuperare l'interfaccia IProvideTaskPage, quindi chiamare IProvideTaskPage GetPage. Il Metodo GetPage restituisce un handle per la pagina, che può quindi essere usato per visualizzare la pagina richiesta.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recupero della pagina di attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046911"
---
# <a name="retrieving-a-task-page-example"></a>Esempio di recupero di una pagina attività

Per recuperare una pagina di attività, è necessario chiamare **ITask:: QueryInterface** per recuperare l'interfaccia [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , quindi chiamare [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). Il metodo **GetPage** restituisce un handle per la pagina, che può quindi essere usato per visualizzare la pagina richiesta.

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Nella procedura riportata di seguito viene descritto come creare un nuovo trigger.

**Per creare un nuovo trigger**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare **ITask:: QueryInterface** per recuperare l'interfaccia [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) per recuperare la pagina.
4.  Usando l'handle di pagina restituito, visualizzare la pagina.



| Per un esempio di codice di                                   | Vedere                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recupero e visualizzazione della pagina attività di un'attività nota | [Recupero di una pagina di attività](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
---
title: Esempio di creazione di un'attività con NewWorkItem
description: Quando si crea un'attività, si utilizzeranno due interfacce Utilità di pianificazione ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- creazione di elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione, creazione di attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338390"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Esempio di creazione di un'attività con NewWorkItem

Quando si crea un'attività, si useranno due interfacce di Utilità di pianificazione: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). È necessario specificare un nome univoco per l'attività, l'identificatore di classe dell'oggetto attività e l'identificatore di interfaccia di **ITask**. L'identificatore di classe e l'identificatore di interfaccia vengono mostrati nell'esempio di codice riportato in questo argomento.

> [!Note]  
> È anche possibile creare un'attività chiamando [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Quando si esegue questa route, è responsabilità della creazione di un'istanza dell'oggetto **attività** , che supporta l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , quindi aggiungere l'attività con il nome fornito.

 

> [!Note]  
> Per impostazione predefinita, solo un membro del gruppo Administrators, Backup Operators o Server Operators può creare attività in Windows Server 2003. Un membro del gruppo Administrators può modificare il descrittore di sicurezza della \\ cartella attività di Windows per consentire ad altri di creare attività.

 

Il nome fornito per l'attività deve essere univoco all'interno della cartella attività pianificate. Se un'attività con lo stesso nome esiste già, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) restituisce il \_ file degli errori \_ . Se si ottiene questo valore restituito, è necessario specificare un nome diverso e tentare di creare nuovamente l'attività.

Nella procedura seguente viene descritto come creare una nuova attività elemento di lavoro.

**Per creare una nuova attività elemento di lavoro**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) per creare una nuova attività. Questo metodo restituisce un puntatore a un'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
3.  Salvare la nuova attività su disco chiamando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia **ITask** .
4.  Chiamare **ITask:: Release** per rilasciare tutte le risorse. Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).



| Per un esempio di codice di  | Vedere                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Creazione di una singola attività | [Esempio di codice C/C++: creazione di un'attività con NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
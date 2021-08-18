---
title: Esempio di creazione di un'attività con NewWorkItem
description: Quando si crea un'attività, si useranno due interfacce Utilità di pianificazione ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- creazione di elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione , creazione di attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d0e0d216c5aaccee6a51cbac939b2b3bfa421338e12d66ffdd3b8cf055862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139584"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Esempio di creazione di un'attività con NewWorkItem

Quando si crea un'attività, si useranno due interfacce Utilità di pianificazione: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). È necessario specificare un nome univoco per l'attività, l'identificatore di classe dell'oggetto attività e l'identificatore di interfaccia **di ITask**. L'identificatore di classe e l'identificatore di interfaccia sono illustrati nell'esempio di codice che segue questo argomento.

> [!Note]  
> È anche possibile creare un'attività chiamando [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Quando si esegue questa route, è responsabilità dell'utente creare un'istanza dell'oggetto **Task** (che supporta l'interfaccia [**ITask)**](/windows/desktop/api/Mstask/nn-mstask-itask) e quindi aggiungere l'attività con il nome specificato.

 

> [!Note]  
> Per impostazione predefinita, solo un membro del gruppo Administrators, Backup Operators o Server Operators può creare attività in Windows Server 2003. Un membro del gruppo Administrators può modificare il descrittore di sicurezza della cartella attività Windows per consentire ad \\ altri utenti di creare attività.

 

Il nome specificato per l'attività deve essere univoco all'interno della cartella Attività pianificate. Se esiste già un'attività con lo stesso nome, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) restituisce ERROR \_ FILE \_ EXISTS. Se si ottiene questo valore restituito, è necessario specificare un nome diverso e provare a creare nuovamente l'attività.

La procedura seguente descrive come creare una nuova attività elemento di lavoro.

**Per creare una nuova attività elemento di lavoro**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) per creare una nuova attività. Questo metodo restituisce un puntatore a [**un'interfaccia ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
3.  Salvare la nuova attività su disco chiamando [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). [**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia COM standard supportata **dall'interfaccia ITask.**
4.  Chiamare **ITask::Release** per rilasciare tutte le risorse. Si noti che [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un [**metodo IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Per un esempio di codice di  | Vedere                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Creazione di una singola attività | [Esempio di codice C/C++: creazione di un'attività usando NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 
---
title: Informazioni di registrazione delle attività
description: Le informazioni di registrazione consentono di identificare un'attività in diversi modi. Ad esempio, un'attività può essere identificata dall'autore, dal modo in cui è stata creata (definita origine attività) e dalla data di registrazione.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- informazioni di registrazione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328308"
---
# <a name="task-registration-information"></a>Informazioni di registrazione delle attività

Le informazioni di registrazione consentono di identificare un'attività in diversi modi. Ad esempio, un'attività può essere identificata dall'autore, dal modo in cui è stata creata (definita origine attività) e dalla data di registrazione.

## <a name="using-registration-information"></a>Uso delle informazioni di registrazione

Le informazioni di registrazione vengono in genere specificate quando l'attività viene creata e quindi utilizzata nei modi seguenti:

-   Visualizzato dall'interfaccia utente di Utilità di pianificazione.
-   Ottiene o imposta tramite script o applicazioni C++.
-   In un ambiente aziendale, usato come criterio di ricerca durante l'enumerazione di tutte le attività registrate.

## <a name="types-of-registration-information"></a>Tipi di informazioni di registrazione

Le informazioni di registrazione delle attività sono definite dalle proprietà dell'oggetto [**RegistrationInfo**](registrationinfo.md) per le applicazioni di scripting, dalle proprietà dell'interfaccia [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) per le applicazioni C++ e dagli elementi figlio dell' [**elemento RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) per la lettura o la scrittura di XML.

Queste proprietà consentono di accedere ai tipi di informazioni di registrazione seguenti:

-   Autore attività

    Utilità di pianificazione imposta l'autore dell'attività al momento della creazione.

-   Data di registrazione attività

    Utilità di pianificazione imposta questa data quando l'attività è registrata.

-   Descrizione dell'attività

    Descrizione definita dall'utente che può includere i trigger usati per avviare l'attività o le azioni eseguite dall'attività.

-   Documentazione delle attività

    Documentazione fornita dall'utente necessaria per l'attività.

-   Descrittore di sicurezza delle attività

    Descrittore di sicurezza fornito dall'utente.

-   Origine attività

    Informazioni fornite dall'utente che descrivono la posizione di origine dell'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.

-   URI attività

    URI (Uniform Resource Identifier) per l'attività.

-   Versione attività

    Informazioni fornite dall'utente utilizzate quando esistono più versioni di un'attività.

-   Testo XML

    Una versione in formato XML delle informazioni di registrazione. Si noti che è possibile impostare o modificare le informazioni di registrazione direttamente tramite questo XML e le proprietà dell'oggetto e dell'interfaccia appropriate verranno aggiornate di conseguenza.

## <a name="registering-tasks"></a>Registrazione di attività

Un'attività può essere registrata dopo la creazione delle definizioni di attività e le informazioni di registrazione e i valori delle impostazioni vengono forniti dall'utente. Un'attività viene registrata usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) per le applicazioni di scripting o il metodo [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) per le applicazioni C++. Se si desidera registrare un'attività utilizzando XML per definire l'attività, utilizzare il metodo [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per le applicazioni di scripting e il metodo [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) per le applicazioni C++.

Nei metodi indicati in precedenza è possibile specificare il contesto di sicurezza per l'esecuzione dell'attività. È necessario essere un amministratore del sistema per pianificare l'esecuzione dei processi in contesti diversi da quelli personalizzati. Per ulteriori informazioni sui contesti di sicurezza per l'esecuzione di attività, vedere [contesti di sicurezza per l'esecuzione di attività](security-contexts-for-running-tasks.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





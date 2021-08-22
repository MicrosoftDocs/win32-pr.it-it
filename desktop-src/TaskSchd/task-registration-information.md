---
title: Informazioni di registrazione attività
description: Le informazioni di registrazione consentono di identificare un'attività in diversi modi. Ad esempio, un'attività può essere identificata dall'autore, dalla modalità di creazione (definita origine dell'attività) e dalla data di registrazione.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- informazioni di registrazione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e3dc9163b1074eff12be6b872780184b112b6c8a2512e3a68901d083f9c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139284"
---
# <a name="task-registration-information"></a>Informazioni di registrazione attività

Le informazioni di registrazione consentono di identificare un'attività in diversi modi. Ad esempio, un'attività può essere identificata dall'autore, dalla modalità di creazione (definita origine dell'attività) e dalla data di registrazione.

## <a name="using-registration-information"></a>Uso delle informazioni di registrazione

Le informazioni di registrazione vengono in genere specificate quando l'attività viene creata e quindi usata nei modi seguenti:

-   Visualizzato dall'interfaccia Utilità di pianificazione utente.
-   Ottiene o imposta in base ad applicazioni o script C++.
-   In un ambiente aziendale, usato come criterio di ricerca durante l'enumerazione di tutte le attività registrate.

## <a name="types-of-registration-information"></a>Tipi di informazioni di registrazione

Le informazioni di registrazione delle attività sono definite dalle proprietà dell'oggetto [**RegistrationInfo**](registrationinfo.md) per lo scripting delle applicazioni, dalle proprietà dell'interfaccia [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) per le applicazioni C++ e dagli elementi figlio dell'elemento [**RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) per la lettura o la scrittura di XML.

Queste proprietà consentono l'accesso ai tipi di informazioni di registrazione seguenti:

-   Autore attività

    Utilità di pianificazione imposta l'autore dell'attività quando viene creata.

-   Data registrazione attività

    Utilità di pianificazione imposta questa data di registrazione dell'attività.

-   Descrizione dell'attività

    Descrizione definita dall'utente che può includere i trigger usati per avviare l'attività o le azioni eseguite dall'attività.

-   Documentazione delle attività

    Documentazione fornita dall'utente necessaria per l'attività.

-   Descrittore di sicurezza delle attività

    Descrittore di sicurezza fornito dall'utente.

-   Origine attività

    Informazioni fornite dall'utente che descrivono l'origine dell'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.

-   URI attività

    URI (Uniform Resource Identifier) per l'attività.

-   Versione attività

    Informazioni fornite dall'utente utilizzate quando esistono più versioni di un'attività.

-   Testo XML

    Versione in formato XML delle informazioni di registrazione. Si noti che è possibile impostare o modificare le informazioni di registrazione direttamente tramite questo codice XML e le proprietà appropriate dell'oggetto e dell'interfaccia verranno aggiornate di conseguenza.

## <a name="registering-tasks"></a>Registrazione di attività

Un'attività può essere registrata dopo la creazione delle definizioni di attività e le informazioni di registrazione e i valori delle impostazioni vengono forniti dall'utente. Un'attività viene registrata usando il [**metodo TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) per lo scripting di applicazioni o il metodo [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) per le applicazioni C++. Se si vuole registrare un'attività usando XML per definire l'attività, usare il metodo [**TaskFolder.RegisterTask**](taskfolder-registertask.md) per lo scripting delle applicazioni e il metodo [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) per le applicazioni C++.

Nei metodi indicati in precedenza è possibile specificare il contesto di sicurezza per eseguire l'attività. È necessario essere un amministratore del sistema per pianificare l'esecuzione dei processi in contesti diversi dal proprio. Per altre informazioni sui contesti di sicurezza per l'esecuzione di attività, vedere [Contesti di sicurezza per l'esecuzione di attività.](security-contexts-for-running-tasks.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





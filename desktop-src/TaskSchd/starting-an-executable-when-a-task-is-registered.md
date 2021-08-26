---
title: Avvio di un eseguibile quando viene registrata un'attività
description: La scrittura di un'attività che avvia un eseguibile quando viene registrata un'attività viene eseguita definendo un trigger di registrazione e un'azione eseguibile.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Utilità di pianificazione esempi Utilità di pianificazione trigger di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a051c820a1099828ae0ee123e4241ec42d6edbb23ce9e98275057b5903dfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033951"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Avvio di un eseguibile quando viene registrata un'attività

La scrittura di un'attività che avvia un eseguibile quando viene registrata un'attività viene eseguita definendo un trigger di registrazione e un'azione eseguibile.

## <a name="registration-trigger"></a>Trigger di registrazione

I trigger di registrazione avviano un'attività non appena viene registrata. È anche possibile specificare un ritardo per il trigger di registrazione, che avvia un'attività dopo un periodo di tempo specifico (ritardo) dopo la registrazione dell'attività. Il ritardo viene specificato nella [**proprietà Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) dell'interfaccia [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger per**](registrationtrigger.md) lo scripting).

> [!Note]  
> Quando viene aggiornata un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.

 

## <a name="registration-trigger-examples"></a>Esempi di trigger di registrazione

Gli esempi seguenti iniziano Blocco note quando viene registrata un'attività:

-   [Esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md)
-   [Esempio di trigger di registrazione (C++)](registration-trigger-example--c---.md)
-   [Esempio di trigger di registrazione (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 





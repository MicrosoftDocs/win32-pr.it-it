---
title: Avvio di un eseguibile quando un'attività è registrata
description: La scrittura di un'attività che avvia un eseguibile quando un'attività viene registrata viene eseguita definendo un trigger di registrazione e un'azione eseguibile.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955583"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Avvio di un eseguibile quando un'attività è registrata

La scrittura di un'attività che avvia un eseguibile quando un'attività viene registrata viene eseguita definendo un trigger di registrazione e un'azione eseguibile.

## <a name="registration-trigger"></a>Trigger di registrazione

I trigger di registrazione avviano un'attività non appena viene registrata. È anche possibile specificare un ritardo per il trigger di registrazione, che avvia un'attività dopo un periodo di tempo specifico, ovvero il ritardo, dopo la registrazione dell'attività. Il ritardo viene specificato nella proprietà [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) dell'interfaccia [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) per lo scripting).

> [!Note]  
> Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.

 

## <a name="registration-trigger-examples"></a>Esempi di trigger di registrazione

Gli esempi seguenti avviano il blocco note quando un'attività è registrata:

-   [Esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md)
-   [Esempio di trigger di registrazione (C++)](registration-trigger-example--c---.md)
-   [Esempio di trigger di registrazione (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 





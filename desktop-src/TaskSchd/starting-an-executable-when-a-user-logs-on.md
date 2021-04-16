---
title: Avvio di un eseguibile quando un utente esegue l'accesso
description: La scrittura di un'attività che avvia un eseguibile quando un utente esegue l'accesso viene eseguita definendo un trigger LOGON e un'azione eseguibile.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger LOGON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395270"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Avvio di un eseguibile quando un utente esegue l'accesso

La scrittura di un'attività che avvia un eseguibile quando un utente esegue l'accesso viene eseguita definendo un trigger LOGON e un'azione eseguibile.

## <a name="logon-trigger"></a>Trigger LOGON

I trigger LOGON vengono attivati dal limite iniziale, ma non avviano l'eseguibile fino a quando un utente specificato non esegue l'accesso. È possibile specificare il trigger LOGON per l'avvio quando un determinato utente accede specificando l'utente nella proprietà [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) dell'interfaccia [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) per lo scripting).

## <a name="logontrigger-examples"></a>Esempi di LogonTrigger

Gli esempi seguenti avviano il blocco note dopo che un utente ha eseguito l'accesso.

-   [Esempio di trigger LOGON (scripting)](logon-trigger-example--scripting-.md)
-   [Esempio di trigger LOGON (C++)](logon-trigger-example--c---.md)
-   [Esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 





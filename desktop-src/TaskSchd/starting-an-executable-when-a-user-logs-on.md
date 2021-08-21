---
title: Avvio di un eseguibile quando un utente accede
description: La scrittura di un'attività che avvia un eseguibile quando un utente accede viene eseguita definendo un trigger di accesso e un'azione eseguibile.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Utilità di pianificazione esempi Utilità di pianificazione trigger di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd7cfc8412e33df47841cf33d2a4950061d39d77fbe76d3b896b5d220b04b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132123"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Avvio di un eseguibile quando un utente accede

La scrittura di un'attività che avvia un eseguibile quando un utente accede viene eseguita definendo un trigger di accesso e un'azione eseguibile.

## <a name="logon-trigger"></a>Trigger di accesso

I trigger di accesso vengono attivati dal limite iniziale, ma non avviano l'eseguibile fino a quando un utente specificato non esegue l'accesso. È possibile specificare il trigger di accesso da avviare quando un determinato utente accede specificando l'utente nella [**proprietà UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) dell'interfaccia [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) per lo scripting).

## <a name="logontrigger-examples"></a>Esempi di LogonTrigger

Gli esempi seguenti iniziano Blocco note dopo l'accesso di un utente.

-   [Esempio di trigger di accesso (scripting)](logon-trigger-example--scripting-.md)
-   [Esempio di trigger di accesso (C++)](logon-trigger-example--c---.md)
-   [Esempio di trigger di accesso (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 





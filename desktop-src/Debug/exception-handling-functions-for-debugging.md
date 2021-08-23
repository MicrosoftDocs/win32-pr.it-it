---
description: Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passando l'eccezione. Questa notifica è nota come notifica first-chance. Il sistema sospende quindi tutti i thread del processo in fase di debug.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funzioni di gestione delle eccezioni per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4542b6e1d3ad2699b3cb43d15e327d26156760980188555b1a4bf9c68e9a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573171"
---
# <a name="exception-handling-functions-for-debugging"></a>Funzioni di gestione delle eccezioni per il debug

Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passando l'eccezione. Questa operazione è nota come *notifica first-chance.* Il sistema sospende quindi tutti i thread del processo in fase di debug.

Se il debugger non gestisce l'eccezione, il sistema tenta di individuare un gestore eccezioni appropriato. Se il sistema non riesce a individuarne uno appropriato, il sistema notifica nuovamente al debugger che si è verificata un'eccezione. Questa operazione è nota come *notifica last-chance.* Se il debugger non gestisce l'eccezione dopo la notifica last-chance, il sistema termina il processo in fase di debug.

Per altre informazioni, vedere [Gestione delle eccezioni del debugger](debugger-exception-handling.md).

 

 




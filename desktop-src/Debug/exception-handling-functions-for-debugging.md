---
description: Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passandovi l'eccezione. Questa operazione è nota come notifica first-chance. Il sistema sospende quindi tutti i thread nel processo di cui è in corso il debug.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funzioni di gestione delle eccezioni per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877161"
---
# <a name="exception-handling-functions-for-debugging"></a>Funzioni di gestione delle eccezioni per il debug

Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passandovi l'eccezione. Questa operazione è nota come *notifica first-chance*. Il sistema sospende quindi tutti i thread nel processo di cui è in corso il debug.

Se il debugger non gestisce l'eccezione, il sistema tenta di individuare un gestore di eccezioni appropriato. Se il sistema non è in grado di individuare un oggetto appropriato, il sistema informa nuovamente il debugger che si è verificata un'eccezione. Questo è noto come *notifica dell'ultima opportunità*. Se il debugger non gestisce l'eccezione dopo la notifica dell'ultima probabilità, il sistema termina il processo di cui è in corso il debug.

Per ulteriori informazioni, vedere [gestione delle eccezioni del debugger](debugger-exception-handling.md).

 

 




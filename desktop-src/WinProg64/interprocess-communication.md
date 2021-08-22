---
title: Comunicazione interprocesso
description: Le tecniche seguenti possono essere usate per la comunicazione tra applicazioni a 32 bit e a 64 bit.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- comunicazione interprocesso a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5089440caf6ac537a314e7e920796fadeac5817220ba91f283c297bd0451b705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734121"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Comunicazione interprocesso tra applicazioni a 32 bit e a 64 bit

Le tecniche seguenti possono essere usate per la comunicazione tra applicazioni a 32 bit e a 64 bit:

-   Le versioni a 64 bit di Windows usano handle a 32 bit per l'interoperabilità. Quando si condivide un handle tra applicazioni a 32 bit e a 64 bit, solo i 32 bit inferiori sono significativi, pertanto è sicuro troncare l'handle (quando lo si passa da 64 bit a 32 bit) o firmare-estendere l'handle (quando lo si passa da 32 bit a 64 bit). Gli handle che possono essere condivisi includono handle a oggetti utente quali finestre (**HWND**), handle a oggetti GDI come penne e pennelli **(HBRUSH** e **HPEN)** e handle a oggetti denominati, ad esempio mutex, semafori e handle di file.
-   È possibile utilizzare rpc (Remote Procedure Call).
-   È possibile usare localServer COM se le DLL proxy/stub a 32 bit e a 64 bit sono registrate per tutte le interfacce usate.
-   La memoria condivisa può essere usata se i tipi dipendenti dal puntatore vengono convertiti correttamente (o evitati).
-   Le [**funzioni CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) possono avviare processi a 32 bit e a 64 bit da processi a 32 bit o a 64 bit con determinate limitazioni.

Non è possibile avviare un file eseguibile a 64 bit in %windir% System32 da un processo a 32 bit, perché il redirector file system reindirizza \\ il percorso. A tale scopo, non disabilitare il reindirizzamento. in alternativa, usare %windir% \\ Sysnative. Per altre informazioni, vedere [Redirector del file system.](file-system-redirector.md)

 

 
---
title: Comunicazione interprocesso
description: Le tecniche seguenti possono essere utilizzate per la comunicazione tra applicazioni a 32 bit e a 64 bit.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- comunicazione interprocesso-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399411"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Comunicazione interprocesso tra applicazioni a 32 bit e 64 bit

Per la comunicazione tra applicazioni a 32 bit e a 64 bit, è possibile usare le tecniche seguenti:

-   le versioni a 64 bit di Windows usano handle a 32 bit per l'interoperabilità. Quando si condivide un handle tra applicazioni a 32 bit e a 64 bit, solo i 32 bit inferiori sono significativi, quindi è possibile troncare il punto di controllo (quando lo si passa da 64 bit a 32 bit) o estendere la firma dell'handle (quando viene passato da 32 a 64 bit). Gli handle che possono essere condivisi includono handle per oggetti utente quali Windows (**HWND**), handle per oggetti GDI quali penne e pennelli (**HBRUSH** e **HPEN**) e handle a oggetti denominati, quali mutex, semafori e handle di file.
-   È possibile utilizzare le chiamate di procedura remota (RPC).
-   LocalServers COM può essere usato se le DLL di proxy/stub a 32 bit e 64 sono registrate per tutte le interfacce usate.
-   È possibile usare la memoria condivisa se i tipi dipendenti dal puntatore vengono convertiti correttamente (o evitati).
-   Le funzioni [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) e [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) possono avviare processi a 32 bit e a 64 bit da processi a 32 bit o a 64 bit con determinate limitazioni.

Impossibile avviare un file eseguibile a 64 bit in% windir% \\ system32 da un processo a 32 bit, perché il redirector file System reindirizza il percorso. Non disabilitare il reindirizzamento per eseguire questa operazione. utilizzare% windir% \\ SysNative in alternativa. Per ulteriori informazioni, vedere [redirector del file System](file-system-redirector.md).

 

 
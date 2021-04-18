---
title: Accesso al registro di sistema remoto in Windows a 64 bit
description: Il redirector del registro di sistema consente l'accesso remoto al registro di sistema in Windows a 64 bit tramite la funzione RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- accesso al registro di sistema remoto a 64 bit programmazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299830"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Accesso al registro di sistema remoto in Windows a 64 bit

Il redirector del registro di sistema consente l'accesso remoto al registro di sistema in Windows a 64 bit tramite la funzione [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Se il client è un'applicazione a 32 bit, accede alla visualizzazione del registro di sistema predefinita a 32 bit del server. Se il client è un'applicazione a 64 bit, accede alla visualizzazione del registro di sistema a 64 bit.

**Windows Server 2003:** Tutti i client accedono alla visualizzazione del registro di sistema a 64 bit, a meno che l'applicazione non usi il \_ \_ flag 32KEY WOW64 chiave. Questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1) e Windows XP Professional x64 Edition, a condizione che sia il client che il server eseguano queste versioni di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del registro di sistema](registry-reflection.md)
</dt> </dl>

 

 
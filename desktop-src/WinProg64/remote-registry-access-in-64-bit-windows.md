---
title: Accesso al Registro di sistema remoto in Windows
description: Il redirector del Registro di sistema fornisce l'accesso remoto al Registro di sistema in Windows a 64 bit tramite la funzione RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- remote registry access 64-bit Windows Programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f066641b080ace60a62c882a4abd0190e20537259517a2e789b4d450e352349
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561452"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Accesso al Registro di sistema remoto in Windows

Il redirector del Registro di sistema fornisce l'accesso remoto al Registro di sistema in Windows a 64 bit tramite la [**funzione RegConnectRegistry.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)

Se il client è un'applicazione a 32 bit, accede alla visualizzazione predefinita del Registro di sistema a 32 bit del server. Se il client è un'applicazione a 64 bit, accede alla visualizzazione del Registro di sistema a 64 bit.

**Windows Server 2003:** Tutti i client accedono alla visualizzazione del Registro di sistema a 64 bit, a meno che l'applicazione non usi il \_ flag KEY WOW64 \_ 32KEY. Questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1) e Windows XP Professional x64 Edition, a condizione che sia il client che il server esee siano in esecuzione queste versioni di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del Registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del Registro di sistema](registry-reflection.md)
</dt> </dl>

 

 
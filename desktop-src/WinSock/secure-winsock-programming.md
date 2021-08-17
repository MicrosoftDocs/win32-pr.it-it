---
description: Di seguito è riportata una guida per proteggere la Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programmazione Winsock sicura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c3644e18a45da4a1d4fa9c20bd2d023ba41d02fed3014f2992c219601bf963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559719"
---
# <a name="secure-winsock-programming"></a>Programmazione Winsock sicura

Di seguito è riportata una guida per proteggere la Windows Sockets. È progettato per offrire una conoscenza della sicurezza Winsock e delle opzioni disponibili per lo sviluppatore di applicazioni di rete sicura.

-   [Uso di SO \_ REUSEADDR e SO \_ EXCLUSIVEADDRUSE](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Estensioni secure socket Winsock](winsock-secure-socket-extensions.md)

Le comunicazioni che usano i socket possono anche essere crittografate usando gli standard SSL/TLS usando il canale sicuro, noto anche come tecnologia Schannel. Schannel è un provider di supporto per la sicurezza (SSP) che contiene un set di protocolli di sicurezza che forniscono l'autenticazione delle identità e la comunicazione privata protetta tramite crittografia. Schannel viene usato principalmente per le applicazioni Internet che richiedono comunicazioni Hypertext Transfer Protocol (HTTP). Per altre informazioni, vedere [Canale sicuro](../secauthn/secure-channel.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Canale sicuro](../secauthn/secure-channel.md)
</dt> </dl>

 

 

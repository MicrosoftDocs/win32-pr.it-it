---
description: Come creare una connessione sicura usando Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Creazione di una connessione protetta tramite Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008909"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Creazione di una connessione protetta tramite Schannel

Il pacchetto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) Schannel fornisce l'accesso a quattro [*protocolli di sicurezza:*](/windows/desktop/SecGloss/s-gly)

-   [Transport Layer Security (TLS 1.2)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1.1)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1.0)](transport-layer-security-protocol.md)
-   [Secure Sockets Layer (SSL 3.0)](secure-sockets-layer-protocol.md)
-   [Secure Sockets Layer (SSL 2.0)](secure-sockets-layer-protocol.md)

> [!Note]  
> I protocolli PCT e SSL 2.0 sono stati sostituiti dal protocollo TLS e non devono essere usati per il nuovo sviluppo.

 

**Per configurare una connessione sicura tra un client e un server**

1.  Ottenere le credenziali Schannel ([Recupero delle credenziali Schannel](obtaining-schannel-credentials.md)).
2.  Creare un contesto di sicurezza Schannel ([Creazione di un contesto di sicurezza Schannel](creating-an-schannel-security-context.md)).

Dopo aver stabilito una connessione, è possibile recuperare informazioni sui relativi attributi. Per informazioni dettagliate, vedere [Recupero di informazioni sulle connessioni Schannel.](getting-information-about-schannel-connections.md)

Se, dopo aver stabilito una connessione, i requisiti di sicurezza dell'applicazione cambiano o la connessione viene persa, è possibile rinegoziare la connessione. Per informazioni dettagliate, [vedere Rinegoziazione di una connessione Schannel.](renegotiating-an-schannel-connection.md)

Al termine dell'uso di una connessione Schannel, è necessario eseguire la pulizia necessaria. Per informazioni dettagliate, vedere [Arresto di una connessione Schannel.](shutting-down-an-schannel-connection.md)

Per informazioni sugli esempi forniti con Platform Software Development Kit (SDK) che illustrano il pacchetto di sicurezza [*Schannel,*](/windows/desktop/SecGloss/s-gly)vedere gli esempi di PSDK con Schannel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica di crittografia schannel e punti di forza di crittografia](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 

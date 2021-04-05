---
description: Come creare una connessione sicura usando Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Creazione di una connessione sicura mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757292"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Creazione di una connessione sicura mediante Schannel

Il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) Schannel fornisce l'accesso a quattro [*protocolli di sicurezza*](/windows/desktop/SecGloss/s-gly):

-   [Transport Layer Security (TLS 1,2)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,1)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,0)](transport-layer-security-protocol.md)
-   [Secure Sockets Layer (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [Secure Sockets Layer (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> I protocolli PCT e SSL 2,0 sono stati sostituiti dal protocollo TLS e non devono essere usati per il nuovo sviluppo.

 

**Per configurare una connessione sicura tra un client e un server**

1.  Ottenere le credenziali Schannel ([ottenendo le credenziali Schannel](obtaining-schannel-credentials.md)).
2.  Creare un contesto di sicurezza Schannel ([creando un contesto di sicurezza Schannel](creating-an-schannel-security-context.md)).

Una volta stabilita una connessione, è possibile recuperare informazioni sugli attributi. Per informazioni dettagliate, vedere [ottenere informazioni sulle connessioni Schannel](getting-information-about-schannel-connections.md).

Se, dopo aver stabilito una connessione, i requisiti di sicurezza dell'applicazione cambiano o la connessione viene persa, è possibile rinegoziare la connessione. Per informazioni dettagliate, vedere [rinegoziazione di una connessione Schannel](renegotiating-an-schannel-connection.md).

Al termine dell'utilizzo di una connessione Schannel, è necessario eseguire la pulizia necessaria. Per informazioni dettagliate, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md).

Per informazioni sugli esempi forniti con Platform Software Development Kit (SDK) che illustrano il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly)Schannel, vedere gli esempi di PSDK con Schannel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specificare le crittografie Schannel e i punti di forza della crittografia](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 

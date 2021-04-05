---
description: Le credenziali sono necessarie per il processo di autenticazione Schannel; sia il client che il server devono ottenere credenziali valide per stabilire un contesto di sicurezza per lo scambio di messaggi. Per un esempio in cui viene illustrata questa procedura, vedere Recupero delle credenziali.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Recupero delle credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756437"
---
# <a name="obtaining-schannel-credentials"></a>Recupero delle credenziali Schannel

Le credenziali sono necessarie per il processo di autenticazione Schannel; sia il client che il server devono ottenere credenziali valide per stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi. Per un esempio in cui viene illustrata questa procedura, vedere [recupero delle credenziali](getting-a-certificate-for-schannel.md).

L'applicazione ottiene le credenziali chiamando la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , che restituisce un handle per le credenziali richieste. Poiché gli handle delle credenziali vengono utilizzati per archiviare le informazioni di configurazione, non è possibile utilizzare lo stesso handle sia per le operazioni sul lato client che sul lato server. Ciò significa che le applicazioni che supportano le connessioni client e server devono ottenere almeno due handle di credenziali.

In Windows XP, una [**struttura \_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) specifica quanto segue:

-   Un protocollo di sicurezza
-   Crittografie consentite
-   Punti di forza di crittografia minimo e massimo
-   Un certificato [*X. 509*](../secgloss/x-gly.md) usato per l'autenticazione, necessario per il server, facoltativo per il client, a meno che il server non richieda l'autenticazione client.

Passare la struttura di [**\_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (tramite il parametro *PAuthData* ) alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Questa funzione restituisce l'handle delle credenziali necessario per stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md).

Per informazioni dettagliate sull'impostazione delle crittografie usate con Schannel, vedere Specifica delle crittografie [Schannel e dei punti di forza di crittografia](specifying-schannel-ciphers-and-cipher-strengths.md).

Per informazioni sui certificati, vedere [funzioni di archivio certificati e](../seccrypto/cryptography-functions.md)certificati.

Per un esempio in cui viene illustrata l'apertura di un [*archivio certificati*](../secgloss/c-gly.md) e l'individuazione di un certificato da usare per l'autenticazione Schannel, vedere [ottenere un certificato](getting-a-certificate-for-schannel.md).

 

 

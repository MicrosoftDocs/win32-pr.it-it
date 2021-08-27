---
description: Le credenziali sono richieste dal processo di autenticazione Schannel. Sia il client che il server devono ottenere credenziali valide per stabilire un contesto di sicurezza per lo scambio di messaggi. Per un esempio che illustra questa procedura, vedere Recupero delle credenziali.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Recupero delle credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216965d5b6fb1b21c36425242f54150112b2dcfb00dd7184c828aba865bbb5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921199"
---
# <a name="obtaining-schannel-credentials"></a>Recupero delle credenziali Schannel

Le credenziali sono richieste dal processo di autenticazione Schannel. Sia il client che il server devono ottenere credenziali valide per stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi. Per un esempio che illustra questa procedura, vedere [Recupero delle credenziali](getting-a-certificate-for-schannel.md).

L'applicazione ottiene le credenziali chiamando la [**funzione AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) che restituisce un handle per le credenziali richieste. Poiché gli handle delle credenziali vengono usati per archiviare le informazioni di configurazione, lo stesso handle non può essere usato sia per le operazioni sul lato client che sul lato server. Ciò significa che le applicazioni che supportano connessioni client e server devono ottenere almeno due handle di credenziali.

In Windows XP, una [**struttura \_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) specifica quanto segue:

-   Un protocollo di sicurezza
-   Crittografia consentita
-   Punti di forza minimi e massimi della crittografia
-   Un [*certificato X.509 usato*](../secgloss/x-gly.md) per l'autenticazione: obbligatorio per il server, facoltativo per il client a meno che il server non ne richiede l'autenticazione client.

Passare la [**struttura \_ SCHANNEL CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (tramite il *parametro pAuthData)* alla [**funzione AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Questa funzione restituisce l'handle delle credenziali necessario per stabilire un [*contesto di sicurezza.*](../secgloss/s-gly.md)

Per informazioni dettagliate sull'impostazione delle crittografia usate con Schannel, vedere [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).

Per informazioni sui certificati, vedere [Funzioni dell'archivio certificati e certificati](../seccrypto/cryptography-functions.md).

Per un esempio che illustra l'apertura di un archivio [*certificati*](../secgloss/c-gly.md) e l'individuazione di un certificato da usare per l'autenticazione Schannel, vedere [Recupero di un certificato](getting-a-certificate-for-schannel.md).

 

 

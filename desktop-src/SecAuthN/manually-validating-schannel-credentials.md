---
description: Viene illustrato come convalidare manualmente le credenziali di Schannel.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Convalida manuale delle credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71ddff50ab674825d8effd1a08477116ee0c654d031e7f353a30c95e4f1249f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787003"
---
# <a name="manually-validating-schannel-credentials"></a>Convalida manuale delle credenziali Schannel

Per impostazione predefinita, Schannel convalida il [*certificato del server*](../secgloss/s-gly.md) chiamando la funzione [**WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) Tuttavia, se questa funzionalità è stata disabilitata utilizzando il flag ISC \_ REQ \_ MANUAL \_ CRED VALIDATION, è necessario convalidare il certificato fornito dal server che sta tentando di stabilire la \_ propria identità.

Per convalidare manualmente il certificato del server, è prima necessario ottenerlo. Usare la [**funzione QueryContextAttributes (Generale)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) e specificare il valore dell'attributo SECPKG \_ ATTR \_ REMOTE \_ CERT \_ CONTEXT. Questo attributo restituisce una [**struttura CERT \_ CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) contenente il certificato fornito dal server. Questo certificato è denominato certificato foglia perché è l'ultimo certificato nella catena di certificati ed è più lontano dal [*certificato radice*](../secgloss/r-gly.md).

Usando il certificato foglia è necessario verificare quanto segue:

-   La catena di certificati è completa e la radice è un certificato di un'autorità [*di certificazione (CA)*](../secgloss/c-gly.md) attendibile.
-   L'ora corrente non supera le date di inizio e fine per ognuno dei certificati nella catena di certificati.
-   Nessuno dei certificati nella catena di certificati è stato revocato.
-   La profondità del certificato foglia non è superiore alla profondità massima consentita specificata nell'estensione del certificato. Questo controllo è necessario solo se è specificata una profondità.
-   L'utilizzo del certificato è corretto, ad esempio un certificato [*client*](../secgloss/c-gly.md) non deve essere usato per autenticare un server.
-   Per l'autenticazione server, l'identità del server contenuta nel certificato foglia del server corrisponde al server che il client sta tentando di contattare. In genere, il client corrisponde a un elemento nel campo Nome soggetto del certificato con l'indirizzo IP o il nome DNS del server.

 

 

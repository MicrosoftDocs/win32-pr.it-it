---
description: La prima funzione CryptoAPI chiamata da un'applicazione che usa qualsiasi API di crittografia è la funzione CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contesti del provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ad2e77178ade8cc286dae1ff7334c89d33e46a63af227503f8e163f7d81cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768633"
---
# <a name="cryptographic-service-provider-contexts"></a>Contesti del provider del servizio di crittografia

La prima [*funzione CryptoAPI*](../secgloss/c-gly.md) chiamata da un'applicazione che usa qualsiasi API di crittografia è [**la funzione CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) Questa funzione restituisce un handle a un CSP specifico che include la specifica di un contenitore [*di chiavi specifico*](../secgloss/k-gly.md) all'interno di CSP. Questo contenitore di chiavi è un contenitore di chiavi richiesto in modo specifico oppure è il contenitore di chiavi predefinito per l'utente attualmente connesso.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) può anche creare un nuovo contenitore di chiavi. Per altre informazioni, vedere [Esempio di programma C: Creazione](example-c-program-creating-a-key-container-and-generating-keys.md) di un contenitore di chiavi e Generazione di chiavi e Programma C di [esempio: uso di CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Un [*provider del servizio di*](../secgloss/c-gly.md) crittografia (CSP) ha sia un nome che un tipo. Ad esempio, il nome di uno dei provider di servizi di crittografia attualmente forniti con il sistema operativo è [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md). Si tratta di un provider [di \_ tipo RSA \_ FULL PROV.](prov-rsa-full.md) Il nome di ogni provider è univoco. il tipo di provider non è .

Quando un'applicazione chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle CSP, specifica un tipo di provider e, facoltativamente, un nome di provider. Se vengono specificati sia un tipo che un nome, la funzione carica il provider CSP con il tipo di provider e il nome del provider corrispondenti. La funzione restituisce l'handle del provider di servizi di configurazione che fornisce l'accesso sia [*a*](../secgloss/k-gly.md) CSP che a un contenitore di chiavi all'interno di CSP.

Quando un'applicazione chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e specifica un tipo di provider ma nessun nome di provider, la funzione cerca un provider denominato, controllando prima un elenco di provider denominati predefiniti associati all'utente connesso e, in caso contrario, da un elenco di provider denominati predefiniti associati al computer. Dopo aver determinato il nome del provider, la funzione **CryptAcquireContext** cerca il provider CSP, lo carica e ne restituisce l'handle.

Al termine dell'uso di un handle CSP, rilasciarlo chiamando la [**funzione CryptReleaseContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

 

 

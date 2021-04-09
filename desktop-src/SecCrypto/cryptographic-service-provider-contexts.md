---
description: La prima funzione CryptoAPI chiamata da un'applicazione che usa le API crittografiche è la funzione CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contesti del provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df20df528b0ba0c385c7ab690436351d918f1521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128799"
---
# <a name="cryptographic-service-provider-contexts"></a>Contesti del provider del servizio di crittografia

La prima funzione [*CryptoAPI*](../secgloss/c-gly.md) chiamata da un'applicazione che usa le API crittografiche è la funzione [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) . Questa funzione restituisce un handle a un particolare CSP che include la specifica di un particolare [*contenitore di chiavi*](../secgloss/k-gly.md) all'interno del CSP. Questo contenitore di chiavi è un contenitore di chiavi richiesto in modo specifico oppure è il contenitore di chiavi predefinito per l'utente attualmente connesso.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) può anche creare un nuovo contenitore di chiavi. Per altre informazioni, vedere [esempio di programma c: creazione di un contenitore di chiavi e generazione di chiavi](example-c-program-creating-a-key-container-and-generating-keys.md) e [programma c di esempio: uso di CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) dispone di un nome e di un tipo. Il nome di uno dei CSP attualmente forniti con il sistema operativo è ad esempio provider del servizio di [crittografia di base Microsoft](microsoft-base-cryptographic-provider.md). Si tratta di un provider di tipo [ \_ \_ completo di prova RSA](prov-rsa-full.md) . Il nome di ciascun provider è univoco. il tipo di provider non è.

Quando un'applicazione chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per ottenere un handle CSP, specifica un tipo di provider e, facoltativamente, un nome di provider. Se vengono specificati sia un tipo che un nome, la funzione carica il CSP con il tipo di provider e il nome del provider corrispondenti. La funzione restituisce l'handle del CSP che fornisce l'accesso al CSP e a un [*contenitore di chiavi*](../secgloss/k-gly.md) all'interno del CSP.

Quando un'applicazione chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e specifica un tipo di provider ma nessun nome di provider, la funzione Cerca un provider denominato, controllando prima di tutto un elenco di provider denominati predefiniti associati all'utente connesso e, in caso di esito negativo, da un elenco di provider denominati predefiniti associati al computer. Una volta determinato il nome del provider, la funzione **CryptAcquireContext** Cerca il CSP per quel provider, lo carica e restituisce il relativo handle.

Al termine dell'utilizzo di un handle CSP, rilasciarlo chiamando la funzione [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) .

 

 

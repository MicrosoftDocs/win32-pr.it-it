---
description: Specifica di crittografia schannel e punti di forza di crittografia
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Specifica di crittografia schannel e punti di forza di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ef036038c3c0f759bdf4f2c2d18f0ac005ac01563d2779c5fcac02999fe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917277"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Specifica di crittografia schannel e punti di forza di crittografia

Per gli scambi di informazioni client/server, il comportamento predefinito di Schannel è negoziare la crittografia migliore disponibile in base a quelle abilitate nel Registro di sistema. Le applicazioni possono limitare i punti di forza di crittografia e crittografia consentiti per una connessione usando i membri della struttura [**\_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) come indicato di seguito:

1.  Impostare il **membro palgSupportedAlgs** su una matrice di [**\_ ID alg**](../seccrypto/alg-id.md) contenente le crittografia consentite. Per altre informazioni, vedere ID di crittografia.
2.  Impostare i **membri dwMinimumCipherStrength** e/o **dwMaximumCipherStrength** sul livello minimo e massimo consentiti. Per altre informazioni, vedere Valori di forza di crittografia.
3.  Passare la [**struttura \_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (tramite il *parametro pAuthData)* in una chiamata alla [**funzione AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Questa funzione restituisce un handle di credenziali.
4.  Specificare l'handle delle credenziali in una chiamata alla funzione [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sul lato client o alla funzione [**AcceptSecurityContext (General) lato**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) server.

## <a name="cipher-ids"></a>ID di crittografia

Il comportamento predefinito di Schannel è richiedere la crittografia migliore disponibile in base alle voci Schannel nel Registro di sistema. Non modificare il Registro di sistema. Le impostazioni contenute per Schannel vengono usate a livello globale e influiranno sulle altre applicazioni. Per l'elenco delle costanti valide, vedere [**ALG \_ ID**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Valori di intensità della crittografia

Questa funzionalità Schannel viene in genere usata per limitare una connessione a crittografia di livello nazionale o di esportazione. I punti di forza nazionali includono 56 e 128 bit, mentre il livello di forza dell'esportazione è limitato a 56 bit. Se si impostano i valori minimo e massimo su zero, Schannel userà tutti i punti di forza di crittografia disponibili.

Usando TLS o SSL 3.0, impostare il membro **dwMinimumCipherStrength** su -1 (negativo) per abilitare i pacchetti di crittografia "Null Cipher", che forniscono firme ma nessuna crittografia. Se **anche dwMaximumCipherStrength** è impostato su -1, verranno abilitate solo le suite "Null Cipher". Questa impostazione è destinata solo allo sviluppo e non deve essere usata nei sistemi di produzione.

## <a name="querying-cipher-information"></a>Esecuzione di query sulle informazioni di crittografia

Per recuperare le impostazioni di complessità della crittografia per una credenziale, chiamare la [**funzione QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) e specificare SECPKG ATTR CIPHER STRENGTHS come parametro \_ \_ \_ *ulAttribute.*

Per recuperare l'elenco di algoritmi supportati per una credenziale, chiamare [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) con SECPKG \_ ATTR \_ SUPPORTED \_ ALGS come *parametro ulAttribute.*

 

 

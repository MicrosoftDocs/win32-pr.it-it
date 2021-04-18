---
description: Specificare le crittografie Schannel e i punti di forza della crittografia
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Specificare le crittografie Schannel e i punti di forza della crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316217"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Specificare le crittografie Schannel e i punti di forza della crittografia

Per gli scambi di informazioni client/server, il comportamento predefinito di Schannel è quello di negoziare la crittografia migliore disponibile in base a quelle abilitate nel registro di sistema. Le applicazioni possono limitare le crittografie e i punti di forza della crittografia consentiti per una connessione usando i membri della struttura di [**\_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) come indicato di seguito:

1.  Impostare il membro **palgSupportedAlgs** su una matrice di [**\_ ID ALG**](../seccrypto/alg-id.md) contenente le crittografie consentite. Per altre informazioni, vedere ID di crittografia.
2.  Impostare i membri **dwMinimumCipherStrength** e/o **dwMaximumCipherStrength** sui punti di forza minimi e massimi consentiti. Per altre informazioni, vedere valori di livello di codifica.
3.  Passare la struttura di [**\_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (per mezzo del parametro *pAuthData* ) in una chiamata alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Questa funzione restituisce un handle di credenziali.
4.  Specificare l'handle delle credenziali in una chiamata alla funzione [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) del lato client o alla funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) sul lato server.

## <a name="cipher-ids"></a>ID crittografia

Il comportamento predefinito di Schannel è quello di richiedere la crittografia migliore disponibile in base alle voci Schannel nel registro di sistema. Non modificare il registro di sistema; le impostazioni contenute per Schannel vengono utilizzate globalmente e influiranno su altre applicazioni. Per l'elenco delle costanti valide, vedere [**\_ ID ALG**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Valori di attendibilità della crittografia

Questa funzionalità Schannel viene in genere usata per limitare una connessione a crittografie nazionali o di esportazione. I punti di forza interni includono 56 e 128 bit, mentre la forza di esportazione è limitata a 56 bit. Se si impostano i valori minimo e massimo su zero Schannel utilizzerà tutti i punti di forza di crittografia disponibili.

Utilizzando TLS o SSL 3,0, impostare il membro **dwMinimumCipherStrength** su-1 (negativo) per abilitare i pacchetti di crittografia "null Encryption", che forniscono le firme ma nessuna crittografia. Se anche **dwMaximumCipherStrength** è impostato su-1, verranno abilitati solo i gruppi "crittografia null". Questa impostazione è destinata solo allo sviluppo e non deve essere usata nei sistemi di produzione.

## <a name="querying-cipher-information"></a>Esecuzione di query sulle informazioni di crittografia

Per recuperare le impostazioni del livello di codifica per una credenziale, chiamare la funzione [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) e specificare SECPKG \_ attr \_ cipher \_ strengths come parametro *ulAttribute* .

Per recuperare l'elenco degli algoritmi supportati per una credenziale, chiamare [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) con SECPKG \_ attr \_ supportato \_ algs come parametro *ulAttribute* .

 

 

---
description: I protocolli supportati e i pacchetti di crittografia possono essere elencati da chiamate a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerazione dei protocolli supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310755"
---
# <a name="enumerating-supported-protocols"></a>Enumerazione dei protocolli supportati

I protocolli supportati e i pacchetti di crittografia possono essere elencati da chiamate a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex. Il \_ valore ENUMALGS di PP \_ funziona come PP \_ ENUMALGS ma restituisce una struttura di [**prova \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) che include informazioni più dettagliate sugli algoritmi supportati dal provider.

Per ulteriori informazioni sui flag di protocollo definiti e sui relativi valori, vedere [flag di protocollo](protocol-flags.md).

Dato che il membro **hCryptProv** è l' [*handle*](../secgloss/h-gly.md) di un [*contesto*](../secgloss/c-gly.md) di crittografia aperto acquisito usando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) con il relativo parametro *dwProvType* impostato su prov \_ RSA \_ Schannel, nell'esempio seguente vengono elencati i nomi di tutti gli algoritmi disponibili in CSP.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



Nella tabella seguente sono elencati alcuni algoritmi restituiti da una tipica parte interna di prove \_ RSA \_ Schannel CSP. Si noti che in questo esempio non è supportata né la crittografia SSL2 SHA né la crittografia DES SSL2.



| Identificatore dell'algoritmo                                                                        | Lunghezza minima chiave | Lunghezza massima della chiave | Protocolli | Nome algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*\_MD5 CALG*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | MD5          |
| [*\_Sha CALG*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | Sha          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| CALG \_ des                                                                                   | 56                 | 56                 | 0x0005    | DES          |



 

Per preparare l'invio di messaggi ClientHello o ServerHello, il motore di protocollo [*Schannel*](../secgloss/s-gly.md) enumera gli algoritmi e le dimensioni delle chiavi supportati dal CSP e compila un elenco internamente dei pacchetti di crittografia supportati.

 

 

---
description: I protocolli e i pacchetti di crittografia supportati possono essere elencati tramite chiamate a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerazione dei protocolli supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d7236fe20901e9feb48e844deceea47e8f5936b9685580a653f1480b3b667c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874431"
---
# <a name="enumerating-supported-protocols"></a>Enumerazione dei protocolli supportati

I protocolli e i pacchetti di crittografia supportati possono essere elencati tramite chiamate a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX. Il valore PP ENUMALGS EX funziona come PP ENUMALGS, ma restituisce una struttura \_ \_ \_ [**PROV \_ ENUMALGS \_ EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) che contiene informazioni più dettagliate sugli algoritmi supportati dal provider.

Per altre informazioni sui flag di protocollo definiti e sui relativi valori, vedere [Flag di protocollo.](protocol-flags.md)

Dato che il membro **hCryptProv** è [](../secgloss/c-gly.md) l'handle di un contesto di crittografia aperto acquisito usando [**CryptAcquireContext con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) il parametro *dwProvType* impostato su PROV RSA SCHANNEL, l'esempio seguente elenca i nomi di tutti gli algoritmi disponibili in [](../secgloss/h-gly.md) \_ \_ CSP.


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



La tabella seguente elenca alcuni algoritmi restituiti da un tipico provider di servizi di configurazione PROV \_ RSA \_ SCHANNEL nazionale. Si noti che né i mac SSL2 SHA né la crittografia DES SSL2 sono supportati dal CSP in questo esempio.



| Identificatore dell'algoritmo                                                                        | Lunghezza minima della chiave | Lunghezza massima della chiave | Protocolli | Nome algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | "MD5"          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | "SHA"          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | "RC4"          |
| CALG \_ DES                                                                                   | 56                 | 56                 | 0x0005    | "DES"          |



 

Per preparare l'invio di messaggi ClientHello o ServerHello, il motore del protocollo [*Schannel*](../secgloss/s-gly.md) enumera gli algoritmi e le dimensioni delle chiavi supportati dal CSP e compila internamente un elenco di pacchetti di crittografia supportati.

 

 

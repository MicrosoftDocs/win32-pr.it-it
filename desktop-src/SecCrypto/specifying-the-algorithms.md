---
description: Dopo aver creato o importato una chiave master, sia RSA/SChannel che Diffie-Hellman/SChannel indicano il CSP del tipo di chiavi di crittografia bulk e di chiavi MAC che verranno derivate dalla chiave master.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Specifica degli algoritmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307666"
---
# <a name="specifying-the-algorithms"></a>Specifica degli algoritmi

Dopo aver creato o importato una [*chiave master*](../secgloss/m-gly.md) , sia [*RSA*](../secgloss/r-gly.md)/Schannel che [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel indicano il [*CSP*](../secgloss/c-gly.md) del tipo di [*chiavi di crittografia bulk*](../secgloss/b-gly.md) e di [*chiavi Mac*](../secgloss/m-gly.md) che verranno derivate dalla chiave master. Nell'esempio seguente vengono specificati questi algoritmi. Lo stesso codice viene usato sia per il client che per il server.


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> Un motore di protocollo [*Schannel*](../secgloss/s-gly.md) non deve specificare gli algoritmi e le dimensioni delle chiavi non supportati dal CSP. Per ulteriori informazioni, vedere [enumerazione dei protocolli supportati](enumerating-supported-protocols.md). Se vengono specificati algoritmi non supportati o dimensioni delle chiavi, la funzione CSP deve avere esito negativo e restituire \_ il \_ codice di errore di dati non validi.

 

 

 

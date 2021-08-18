---
description: L'installazione di nuove funzionalità in memoria può migliorare le prestazioni. Le funzioni CryptoAPI cercano la funzionalità nella memoria prima di cercare la DLL nel Registro di sistema. La DLL deve essere caricata prima di installare la funzionalità.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Installazione della nuova funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c71167f8226ad78f449b3f529e2e22bdb060bc0c5d984671cf4c5a30cc6f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005299"
---
# <a name="installing-the-new-functionality"></a>Installazione della nuova funzionalità

L'installazione di nuove funzionalità in memoria può migliorare le prestazioni. [*Le funzioni CryptoAPI*](../secgloss/c-gly.md) cercano la funzionalità nella memoria prima di cercare la DLL nel Registro di sistema. La DLL deve essere caricata prima di installare la funzionalità.

[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installa l'indirizzo della nuova funzionalità. Deve essere inserito nella **funzione DllMain** della DLL.

Se *hModule viene* passato a [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), dopo l'installazione, la DLL non viene scaricata fino a quando Crypt32.dll non viene scaricato.

Nell'esempio seguente viene chiamata [**la funzione CryptInstallOIDFunctionAddress.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 

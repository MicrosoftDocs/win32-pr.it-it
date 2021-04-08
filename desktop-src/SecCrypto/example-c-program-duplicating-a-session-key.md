---
description: Nell'esempio seguente viene creata una chiave di sessione casuale, viene duplicata la chiave, vengono impostati alcuni parametri aggiuntivi sulla chiave originale e vengono eliminate sia le chiavi originali che quelle duplicate.
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 'Esempio di programma C: duplicazione di una chiave di sessione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38934d399a6a38f14e551e79d4e1f877dbadf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967382"
---
# <a name="example-c-program-duplicating-a-session-key"></a>Esempio di programma C: duplicazione di una chiave di sessione

Nell'esempio seguente viene creata una [*chiave di sessione*](../secgloss/s-gly.md)casuale, viene duplicata la chiave, vengono impostati alcuni parametri aggiuntivi sulla chiave originale e vengono eliminate sia le chiavi originali che quelle duplicate. Questo esempio illustra l'uso di [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) e delle funzioni correlate.

In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:

-   Accesso a un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) utilizzando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Creazione di una chiave di sessione mediante [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).
-   Duplicazione della chiave creata con [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey).
-   Uso di [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) per modificare il processo di generazione delle chiavi in due modi diversi.
-   Riempimento di un buffer con byte casuali tramite [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).
-   Eliminazione delle chiavi tramite [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).
-   Rilascio del CSP con [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).

In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md). Il codice per questa funzione è incluso nell'esempio. Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(    
   &hCryptProv,
   NULL,
   NULL,
   PROV_RSA_FULL,
   0)) 
{    
    printf("CryptAcquireContext succeeded. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 

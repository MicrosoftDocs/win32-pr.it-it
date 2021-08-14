---
description: CNG consente di crittografare i dati usando un numero minimo di chiamate di funzione e consente di eseguire tutta la gestione della memoria.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Crittografia dei dati con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b264518c2a0ccfe0f626c869ba3062c0429941234ca0c286f9e7801961485b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907739"
---
# <a name="encrypting-data-with-cng"></a>Crittografia dei dati con CNG

L'uso principale di qualsiasi API di crittografia è la crittografia e la decrittografia dei dati. CNG consente di crittografare i dati usando un numero minimo di chiamate di funzione e consente di eseguire tutta la gestione della memoria. Anche se molti dei dettagli di implementazione del protocollo vengono lasciati all'utente, CNG fornisce le primitive che eseguono le attività effettive di crittografia e decrittografia dei dati.

-   [Crittografia dei dati](#encrypting-data-with-cng)
-   [Esempio di crittografia dei dati](#encrypting-data-example)
-   [Decrittografia di dati](#decrypting-data)

## <a name="encrypting-data"></a>Crittografia dei dati

Per crittografare i dati, seguire questa procedura:

1.  Aprire un provider di algoritmi che supporta la crittografia, ad esempio **BCRYPT \_ DES \_ ALGORITHM.**
2.  Creare una chiave con cui crittografare i dati. È possibile creare una chiave usando una delle funzioni seguenti:
    -   [**BCryptGenerateKeyPair o**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) per i provider asimmetrici.
    -   [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) o [**BCryptImportKey per**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) i provider simmetrici.

    > [!Note]  
    > La crittografia e la decrittografia dei dati con una chiave asimmetrica sono a elevato utilizzo di calcolo rispetto alla crittografia a chiave simmetrica. Se è necessario crittografare i dati con una chiave asimmetrica, è necessario crittografare i dati con una chiave simmetrica, crittografare la chiave simmetrica con una chiave asimmetrica e includere la chiave simmetrica crittografata con il messaggio. Il destinatario può quindi decrittografare la chiave simmetrica e utilizzare la chiave simmetrica per decrittografare i dati.

     

3.  Ottenere le dimensioni dei dati crittografati. Si basa sull'algoritmo di crittografia, sullo schema di riempimento (se presente) e sulle dimensioni dei dati da crittografare. È possibile ottenere le dimensioni dei dati crittografati usando la [**funzione BCryptEncrypt,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) passando **NULL** per *il parametro pbOutput.* Tutti gli altri parametri devono essere uguali a quando i dati vengono effettivamente crittografati, ad eccezione del parametro *pbInput,* che in questo caso non viene usato.
4.  È possibile crittografare i dati sul posto con lo stesso buffer o crittografare i dati in un buffer separato.

    Per crittografare i dati sul posto, passare il puntatore del buffer di testo non crittografato per entrambi i parametri *pbInput* *e pbOutput* nella [**funzione BCryptEncrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) È possibile che le dimensioni dei dati crittografati siano maggiori delle dimensioni dei dati non crittografati, quindi il buffer di testo non crittografato deve essere sufficientemente grande da contenere i dati crittografati, non solo il testo non crittografato. È possibile usare le dimensioni ottenute nel passaggio 3 per allocare il buffer di testo non crittografato.

    Se si desidera crittografare i dati in un buffer separato, allocare un buffer di memoria per i dati crittografati usando le dimensioni ottenute nel passaggio 3.

5.  Chiamare la [**funzione BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) per crittografare i dati. Questa funzione scriverà i dati crittografati nella posizione specificata nel *parametro pbOutput.*
6.  Rendere persistenti i dati crittografati in base alle esigenze.
7.  Ripetere i passaggi 5 e 6 fino a quando tutti i dati non sono stati crittografati.

## <a name="encrypting-data-example"></a>Esempio di crittografia dei dati

Nell'esempio seguente viene illustrato come crittografare i dati con CNG usando l'algoritmo di crittografia simmetrica standard di crittografia avanzata.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a>Decrittografia di dati

Per decrittografare i dati, seguire questa procedura:

1.  Aprire un provider di algoritmi che supporta la crittografia, ad esempio **BCRYPT \_ DES \_ ALGORITHM.**
2.  Ottenere la chiave con cui sono stati crittografati i dati e usarla per ottenere un handle per la chiave.
3.  Ottenere le dimensioni dei dati decrittografati. Si basa sull'algoritmo di crittografia, sullo schema di riempimento (se presente) e sulle dimensioni dei dati da decrittografare. È possibile ottenere le dimensioni dei dati crittografati usando la [**funzione BCryptDecrypt,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) passando **NULL** per *il parametro pbOutput.* I parametri che specificano [](/windows/desktop/SecGloss/i-gly) lo schema di riempimento e il vettore di inizializzazione (IV) devono essere gli stessi di quando i dati sono stati crittografati, ad eccezione del *parametro pbInput,* che in questo caso non viene usato.
4.  Allocare un buffer di memoria per i dati decrittografati.
5.  È possibile decrittografare i dati sul posto usando lo stesso buffer o decrittografare i dati in un buffer separato.

    Per decrittografare i dati sul posto, passare il puntatore del buffer del testo crittografato per entrambi i parametri *pbInput* e *pbOutput* nella [**funzione BCryptDecrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)

    Se si desidera decrittografare i dati in un buffer separato, allocare un buffer di memoria per i dati decrittografati usando le dimensioni ottenute nel passaggio 3.

6.  Chiamare la [**funzione BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) per decrittografare i dati. I parametri che specificano lo schema di riempimento e il vettore di inizializzazione devono essere gli stessi di quando i dati sono stati crittografati. Questa funzione scriverà i dati decrittografati nel percorso specificato nel *parametro pbOutput.*
7.  Rendere persistenti i dati decrittografati in base alle esigenze.
8.  Ripetere i passaggi 5 e 6 fino a quando tutti i dati non sono stati decrittografati.

 

 

---
description: CNG consente di crittografare i dati usando un numero minimo di chiamate di funzione e consente di eseguire tutte le operazioni di gestione della memoria.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Crittografia dei dati con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305604"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="2defe-103">Crittografia dei dati con CNG</span><span class="sxs-lookup"><span data-stu-id="2defe-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="2defe-104">L'uso principale di qualsiasi API di crittografia consiste nel crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="2defe-105">CNG consente di crittografare i dati usando un numero minimo di chiamate di funzione e consente di eseguire tutte le operazioni di gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="2defe-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="2defe-106">Sebbene molti dei dettagli di implementazione del protocollo vengano lasciati all'utente, CNG fornisce le primitive che eseguono le attività effettive di crittografia e decrittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="2defe-107">Crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="2defe-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="2defe-108">Esempio di crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="2defe-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="2defe-109">Decrittografia di dati</span><span class="sxs-lookup"><span data-stu-id="2defe-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="2defe-110">Crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="2defe-110">Encrypting Data</span></span>

<span data-ttu-id="2defe-111">Per crittografare i dati, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="2defe-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2defe-112">Aprire un provider di algoritmi che supporta la crittografia, ad esempio **BCRYPT \_ des \_ Algorithm**.</span><span class="sxs-lookup"><span data-stu-id="2defe-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2defe-113">Creare una chiave con cui crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="2defe-114">È possibile creare una chiave utilizzando una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2defe-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="2defe-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) o [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) per provider asimmetrici.</span><span class="sxs-lookup"><span data-stu-id="2defe-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="2defe-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) o [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) per i provider simmetrici.</span><span class="sxs-lookup"><span data-stu-id="2defe-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="2defe-117">La crittografia e la decrittografia dei dati con una chiave asimmetrica sono a elevato utilizzo di calcolo rispetto alla crittografia della chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="2defe-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="2defe-118">Se è necessario crittografare i dati con una chiave asimmetrica, è necessario crittografare i dati con una chiave simmetrica, crittografare la chiave simmetrica con una chiave asimmetrica e includere la chiave simmetrica crittografata con il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2defe-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="2defe-119">Il destinatario può quindi decrittografare la chiave simmetrica e utilizzare la chiave simmetrica per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="2defe-120">Ottenere le dimensioni dei dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="2defe-121">Si basa sull'algoritmo di crittografia, sullo schema di riempimento (se presente) e sulle dimensioni dei dati da crittografare.</span><span class="sxs-lookup"><span data-stu-id="2defe-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="2defe-122">È possibile ottenere le dimensioni dei dati crittografati tramite la funzione [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) , passando **null** per il parametro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="2defe-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2defe-123">Tutti gli altri parametri devono essere uguali a quelli di quando i dati sono effettivamente crittografati, ad eccezione del parametro *pbInput* , che non viene usato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="2defe-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2defe-124">È possibile crittografare i dati sul posto con lo stesso buffer o crittografare i dati in un buffer separato.</span><span class="sxs-lookup"><span data-stu-id="2defe-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2defe-125">Se si desidera crittografare i dati sul posto, passare il puntatore del buffer di testo non crittografato per i parametri *pbInput* e *PbOutput* nella funzione [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="2defe-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="2defe-126">È possibile che le dimensioni dei dati crittografati siano maggiori delle dimensioni dei dati non crittografati, pertanto il buffer di testo normale deve essere sufficientemente grande da contenere i dati crittografati, non solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="2defe-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="2defe-127">È possibile utilizzare le dimensioni ottenute nel passaggio 3 per allocare il buffer di testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="2defe-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="2defe-128">Se si desidera crittografare i dati in un buffer separato, allocare un buffer di memoria per i dati crittografati utilizzando le dimensioni ottenute nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="2defe-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="2defe-129">Chiamare la funzione [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="2defe-130">Questa funzione scriverà i dati crittografati nel percorso specificato nel parametro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="2defe-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="2defe-131">Salva i dati crittografati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2defe-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="2defe-132">Ripetere i passaggi 5 e 6 fino a quando tutti i dati non sono stati crittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="2defe-133">Esempio di crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="2defe-133">Encrypting Data Example</span></span>

<span data-ttu-id="2defe-134">Nell'esempio seguente viene illustrato come crittografare i dati con CNG utilizzando l'algoritmo di crittografia simmetrica Advanced Encryption Standard.</span><span class="sxs-lookup"><span data-stu-id="2defe-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


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



## <a name="decrypting-data"></a><span data-ttu-id="2defe-135">Decrittografia di dati</span><span class="sxs-lookup"><span data-stu-id="2defe-135">Decrypting Data</span></span>

<span data-ttu-id="2defe-136">Per decrittografare i dati, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="2defe-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="2defe-137">Aprire un provider di algoritmi che supporta la crittografia, ad esempio **BCRYPT \_ des \_ Algorithm**.</span><span class="sxs-lookup"><span data-stu-id="2defe-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="2defe-138">Ottenere la chiave con cui sono stati crittografati i dati e utilizzare tale chiave per ottenere un handle per la chiave.</span><span class="sxs-lookup"><span data-stu-id="2defe-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="2defe-139">Ottenere le dimensioni dei dati decrittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="2defe-140">Si basa sull'algoritmo di crittografia, sullo schema di riempimento (se presente) e sulle dimensioni dei dati da decrittografare.</span><span class="sxs-lookup"><span data-stu-id="2defe-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="2defe-141">È possibile ottenere le dimensioni dei dati crittografati tramite la funzione [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , passando **null** per il parametro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="2defe-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="2defe-142">I parametri che specificano lo schema di riempimento e il [*vettore di inizializzazione*](/windows/desktop/SecGloss/i-gly) (IV) devono essere uguali a quelli della crittografia dei dati, ad eccezione del parametro *pbInput* , che non viene usato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="2defe-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="2defe-143">Allocare un buffer di memoria per i dati decrittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="2defe-144">È possibile decrittografare i dati sul posto usando lo stesso buffer o decrittografare i dati in un buffer separato.</span><span class="sxs-lookup"><span data-stu-id="2defe-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="2defe-145">Per decrittografare i dati sul posto, passare il puntatore del buffer del testo crittografato per i parametri *pbInput* e *PbOutput* nella funzione [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="2defe-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="2defe-146">Se si desidera decrittografare i dati in un buffer separato, allocare un buffer di memoria per i dati decrittografati utilizzando le dimensioni ottenute nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="2defe-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="2defe-147">Chiamare la funzione [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="2defe-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="2defe-148">I parametri che specificano lo schema di riempimento e il vettore di inizializzazione devono essere uguali a quelli dei dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="2defe-149">Questa funzione scriverà i dati decrittografati nel percorso specificato nel parametro *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="2defe-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="2defe-150">Salvare in modo permanente i dati decrittografati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2defe-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="2defe-151">Ripetere i passaggi 5 e 6 fino a quando tutti i dati non vengono decrittografati.</span><span class="sxs-lookup"><span data-stu-id="2defe-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 

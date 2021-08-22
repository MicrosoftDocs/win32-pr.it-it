---
description: Gli hash sono particolarmente utili per verificare l'integrità dei dati quando vengono usati con un algoritmo di firma asimmetrico.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Creazione di un hash con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57d56c4be7dc2f947dbb1869e63fb1789f57e9b4fe6b3a7a06e3cce15580ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907820"
---
# <a name="creating-a-hash-with-cng"></a>Creazione di un hash con CNG

Un [*hash*](/windows/desktop/SecGloss/h-gly) è un'operazione unidirede eseguita su un blocco di dati per creare un valore hash univoco che rappresenta il contenuto dei dati. Indipendentemente dal momento in cui viene eseguito l'hash, lo stesso algoritmo [*hash*](/windows/desktop/SecGloss/h-gly) eseguito sugli stessi dati produrrà sempre lo stesso valore hash. Se uno dei dati cambia, il valore hash cambierà in modo appropriato.

Gli hash non sono utili per la crittografia dei dati perché non sono destinati a essere usati per riprodurre i dati originali dal valore hash. Gli hash sono particolarmente utili per verificare l'integrità dei dati quando vengono usati con un algoritmo di firma asimmetrico. Ad esempio, se è stato eseguito l'hash di un messaggio di testo, l'hash è stato firmato e il valore hash firmato è stato incluso con il messaggio originale, il destinatario potrebbe verificare l'hash firmato, creare il valore hash per il messaggio ricevuto e quindi confrontare questo valore hash con il valore hash firmato incluso nel messaggio originale. Se i due valori hash sono identici, il destinatario può essere ragionevolmente sicuro che il messaggio originale non sia stato modificato.

Le dimensioni del valore hash sono fisse per un particolare algoritmo hash. Ciò significa che, indipendentemente dalla dimensione del blocco di dati, il valore hash avrà sempre le stesse dimensioni. Ad esempio, l'algoritmo hash SHA256 ha una dimensione del valore hash di 256 bit.

-   [Creazione di un oggetto hash](#creating-a-hashing-object)
-   [Creazione di un oggetto hash riutilizzabile](#creating-a-reusable-hashing-object)
-   [Duplicazione di un oggetto hash](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Creazione di un oggetto hash

Per creare un hash usando CNG, seguire questa procedura:

1.  Aprire un provider di algoritmi che supporti l'algoritmo desiderato. Gli algoritmi hash tipici includono MD2, MD4, MD5, SHA-1 e SHA256. Chiamare la [**funzione BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel *parametro pszAlgId.* La funzione restituisce un handle al provider.
2.  Per creare l'oggetto hash, seguire questa procedura:

    1.  Ottenere le dimensioni dell'oggetto chiamando la [**funzione BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la **proprietà BCRYPT OBJECT \_ \_ LENGTH.**
    2.  Allocare memoria per contenere l'oggetto hash.
    3.  Creare l'oggetto chiamando la [**funzione BCryptCreateHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)

3.  Hash dei dati. Ciò comporta la chiamata [**alla funzione BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) una o più volte. Ogni chiamata aggiunge i dati specificati all'hash.
4.  Per ottenere il valore hash, seguire questa procedura:

    1.  Recuperare le dimensioni del valore chiamando la [**funzione BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la **proprietà BCRYPT HASH \_ \_ LENGTH.**
    2.  Allocare memoria per contenere il valore.
    3.  Recuperare il valore hash chiamando la [**funzione BCryptFinishHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) Dopo la chiamata a questa funzione, l'oggetto hash non è più valido.

5.  Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:

    1.  Chiudere l'oggetto hash passando l'handle hash alla [**funzione BCryptDestroyHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash)
    2.  Liberare la memoria allocata per l'oggetto hash.
    3.  Se non verranno creati altri oggetti hash, chiudere il provider di algoritmi passando l'handle del provider alla [**funzione BCryptCloseAlgorithmProvider.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider)

        Se si creeranno più oggetti hash, è consigliabile riutilizzare il provider di algoritmi anziché creare ed eliminare lo stesso tipo di provider di algoritmi più volte.

    4.  Al termine dell'uso della memoria del valore hash, liberarla.

L'esempio seguente illustra come creare un valore hash usando CNG.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

}

```



## <a name="creating-a-reusable-hashing-object"></a>Creazione di un oggetto hash riutilizzabile

A partire da Windows 8 e Windows Server 2012, è possibile creare un oggetto hash riutilizzabile per scenari che richiedono il calcolo di più hash o HMAC in rapida successione. A tale scopo, specificare **BCRYPT \_ HASH \_ REUSABLE \_ FLAG** quando si chiama la [**funzione BCryptOpenAlgorithmProvider.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) Tutti i provider di algoritmi hash Microsoft supportano questo flag. Un oggetto hash creato usando questo flag può essere riutilizzato immediatamente dopo aver chiamato [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) come se fosse stato appena creato chiamando [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Seguire questa procedura per creare un oggetto hash riutilizzabile:

1.  Aprire un provider di algoritmi che supporta l'algoritmo hash desiderato. Chiamare la [**funzione BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel parametro *pszAlgId* e **BCRYPT \_ HASH \_ REUSABLE \_ FLAG** nel *parametro dwFlags.* La funzione restituisce un handle al provider.
2.  Per creare l'oggetto hash, seguire questa procedura:

    1.  Ottenere le dimensioni dell'oggetto chiamando la [**funzione BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la **proprietà BCRYPT OBJECT \_ \_ LENGTH.**
    2.  Allocare memoria per contenere l'oggetto hash.
    3.  Creare l'oggetto chiamando la [**funzione BCryptCreateHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) Specificare **BCRYPT \_ HASH \_ REUSABLE \_ FLAG** nel *parametro dwFlags.*

3.  Hash dei dati chiamando la [**funzione BCryptHashData.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata)
4.  Per ottenere il valore hash, seguire questa procedura:

    1.  Ottenere le dimensioni del valore hash chiamando la [**funzione BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la **proprietà BCRYPT HASH \_ \_ LENGTH.**
    2.  Allocare memoria per contenere il valore.
    3.  Ottenere il valore hash chiamando [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Per riutilizzare l'oggetto hash con nuovi dati, andare al passaggio 3.
6.  Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:

    1.  Chiudere l'oggetto hash passando l'handle hash alla [**funzione BCryptDestroyHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash)
    2.  Liberare la memoria allocata per l'oggetto hash.
    3.  Se non verranno creati altri oggetti hash, chiudere il provider di algoritmi passando l'handle del provider alla [**funzione BCryptCloseAlgorithmProvider.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider)
    4.  Al termine dell'uso della memoria del valore hash, liberarla.

## <a name="duplicating-a-hash-object"></a>Duplicazione di un oggetto hash

In alcuni casi, può essere utile eseguire l'hashing di una quantità di dati comuni e quindi creare due oggetti hash separati dai dati comuni. A tale scopo, non è necessario creare due oggetti hash separati ed eseguire l'hashing dei dati comuni due volte. È possibile creare un singolo oggetto hash e aggiungere tutti i dati comuni all'oggetto hash. È quindi possibile usare la [**funzione BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) per creare un duplicato dell'oggetto hash originale. L'oggetto hash duplicato contiene tutte le stesse informazioni sullo stato e i dati con hash dell'originale, ma è un oggetto hash completamente indipendente. È ora possibile aggiungere i dati univoci a ognuno degli oggetti hash e ottenere il valore hash, come illustrato nell'esempio. Questa tecnica è utile quando si esegue l'hashing di una quantità possibilmente grande di dati comuni. È necessario aggiungere i dati comuni all'hash originale una sola volta e quindi duplicare l'oggetto hash per ottenere un oggetto hash univoco.

 

 

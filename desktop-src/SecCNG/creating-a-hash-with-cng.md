---
description: Gli hash sono particolarmente utili per verificare l'integrità dei dati quando vengono utilizzati con un algoritmo di firma asimmetrica.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Creazione di un hash con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305606"
---
# <a name="creating-a-hash-with-cng"></a>Creazione di un hash con CNG

Un [*hash*](/windows/desktop/SecGloss/h-gly) è un'operazione unidirezionale eseguita su un blocco di dati per creare un valore hash univoco che rappresenta il contenuto dei dati. Indipendentemente dall'esecuzione dell'hash, lo stesso [*algoritmo di hashing*](/windows/desktop/SecGloss/h-gly) eseguito sugli stessi dati produrrà sempre lo stesso valore hash. In caso di modifica dei dati, il valore hash cambierà in modo appropriato.

Gli hash non sono utili per la crittografia dei dati perché non sono destinati a essere usati per riprodurre i dati originali dal valore hash. Gli hash sono particolarmente utili per verificare l'integrità dei dati quando vengono utilizzati con un algoritmo di firma asimmetrica. Se, ad esempio, è stato eseguito l'hashing di un messaggio di testo, la firma dell'hash e il valore hash firmato è stato incluso nel messaggio originale, il destinatario potrebbe verificare l'hash firmato, creare il valore hash per il messaggio ricevuto, quindi confrontare il valore hash con il valore hash firmato incluso nel messaggio originale. Se i due valori hash sono identici, il destinatario può essere ragionevolmente sicuro che il messaggio originale non sia stato modificato.

Le dimensioni del valore hash sono fisse per un algoritmo di hash specifico. Ciò significa che, indipendentemente dalla dimensione del blocco di dati, il valore hash sarà sempre dello stesso tipo. Ad esempio, l'algoritmo di hash SHA256 ha una dimensione del valore hash di 256 bit.

-   [Creazione di un oggetto hash](#creating-a-hashing-object)
-   [Creazione di un oggetto di hashing riutilizzabile](#creating-a-reusable-hashing-object)
-   [Duplicazione di un oggetto hash](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Creazione di un oggetto hash

Per creare un hash con CNG, seguire questa procedura:

1.  Aprire un provider di algoritmi che supporta l'algoritmo desiderato. Gli algoritmi di hash tipici includono MD2, MD4, MD5, SHA-1 e SHA256. Chiamare la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel parametro *pszAlgId* . La funzione restituisce un handle per il provider.
2.  Per creare l'oggetto hash, attenersi alla procedura seguente:

    1.  Ottenere le dimensioni dell'oggetto chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la proprietà della **\_ \_ lunghezza dell'oggetto BCRYPT** .
    2.  Allocare memoria per conservare l'oggetto hash.
    3.  Creare l'oggetto chiamando la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .

3.  Hash dei dati. Questa operazione comporta la chiamata della funzione [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) una o più volte. Ogni chiamata accoda i dati specificati all'hash.
4.  Per ottenere il valore hash, seguire questa procedura:

    1.  Recuperare le dimensioni del valore chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la proprietà **BCRYPT \_ hash \_ length** .
    2.  Allocare memoria per conservare il valore.
    3.  Recuperare il valore hash chiamando la funzione [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) . Dopo che questa funzione è stata chiamata, l'oggetto hash non è più valido.

5.  Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:

    1.  Chiudere l'oggetto hash passando l'handle hash alla funzione [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Liberare la memoria allocata per l'oggetto hash.
    3.  Se non si intende creare altri oggetti hash, chiudere il provider dell'algoritmo passando l'handle del provider alla funzione [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .

        Se si creano più oggetti hash, è consigliabile riutilizzare il provider dell'algoritmo anziché creare ed eliminare più volte lo stesso tipo di provider di algoritmi.

    4.  Al termine dell'utilizzo della memoria per il valore hash, liberare la memoria.

Nell'esempio seguente viene illustrato come creare un valore hash utilizzando CNG.


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



## <a name="creating-a-reusable-hashing-object"></a>Creazione di un oggetto di hashing riutilizzabile

A partire da Windows 8 e Windows Server 2012, è possibile creare un oggetto hash riutilizzabile per gli scenari in cui è necessario calcolare più hash o HMAC in rapida successione. A tale scopo, specificare **il \_ \_ \_ flag BCRYPT hash riutilizzabile** quando si chiama la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) . Tutti i provider di algoritmi hash Microsoft supportano questo flag. Un oggetto hash creato mediante questo flag può essere riutilizzato immediatamente dopo la chiamata a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) come se fosse stato appena creato chiamando [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Per creare un oggetto hash riutilizzabile, attenersi alla procedura seguente:

1.  Aprire un provider di algoritmi che supporta l'algoritmo di hashing desiderato. Chiamare la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel parametro *pszAlgId* e **nel \_ \_ \_ flag BCRYPT hash riutilizzabile** nel parametro *dwFlags* . La funzione restituisce un handle per il provider.
2.  Per creare l'oggetto hash, attenersi alla procedura seguente:

    1.  Ottenere le dimensioni dell'oggetto chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la proprietà della **\_ \_ lunghezza dell'oggetto BCRYPT** .
    2.  Allocare memoria per conservare l'oggetto hash.
    3.  Creare l'oggetto chiamando la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Specificare **il \_ \_ \_ flag BCRYPT hash riutilizzabile** nel parametro *dwFlags* .

3.  Hash dei dati chiamando la funzione [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .
4.  Per ottenere il valore hash, seguire questa procedura:

    1.  Ottenere la dimensione del valore hash chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la proprietà **BCRYPT \_ hash \_ length** .
    2.  Allocare memoria per conservare il valore.
    3.  Ottenere il valore hash chiamando [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Per riutilizzare l'oggetto hash con nuovi dati, andare al passaggio 3.
6.  Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:

    1.  Chiudere l'oggetto hash passando l'handle hash alla funzione [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Liberare la memoria allocata per l'oggetto hash.
    3.  Se non si intende creare altri oggetti hash, chiudere il provider dell'algoritmo passando l'handle del provider alla funzione [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .
    4.  Al termine dell'utilizzo della memoria per il valore hash, liberare la memoria.

## <a name="duplicating-a-hash-object"></a>Duplicazione di un oggetto hash

In alcuni casi può essere utile eseguire l'hashing di una quantità di dati comuni e quindi creare due oggetti hash distinti dai dati comuni. Per eseguire questa operazione, non è necessario creare due oggetti hash distinti ed eseguire l'hashing dei dati comuni due volte. È possibile creare un singolo oggetto hash e aggiungere tutti i dati comuni all'oggetto hash. Quindi, è possibile usare la funzione [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) per creare un duplicato dell'oggetto hash originale. L'oggetto hash duplicato contiene tutte le stesse informazioni sullo stato e i dati con hash dell'originale, ma si tratta di un oggetto hash completamente indipendente. È ora possibile aggiungere i dati univoci a ognuno degli oggetti hash e ottenere il valore hash come illustrato nell'esempio. Questa tecnica è utile quando si esegue l'hashing di una quantità probabilmente elevata di dati comuni. È necessario solo aggiungere i dati comuni all'hash originale una volta, quindi è possibile duplicare l'oggetto hash per ottenere un oggetto hash univoco.

 

 

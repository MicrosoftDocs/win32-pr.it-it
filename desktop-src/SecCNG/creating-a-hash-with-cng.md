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
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="67af9-103">Creazione di un hash con CNG</span><span class="sxs-lookup"><span data-stu-id="67af9-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="67af9-104">Un [*hash*](/windows/desktop/SecGloss/h-gly) è un'operazione unidirezionale eseguita su un blocco di dati per creare un valore hash univoco che rappresenta il contenuto dei dati.</span><span class="sxs-lookup"><span data-stu-id="67af9-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="67af9-105">Indipendentemente dall'esecuzione dell'hash, lo stesso [*algoritmo di hashing*](/windows/desktop/SecGloss/h-gly) eseguito sugli stessi dati produrrà sempre lo stesso valore hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="67af9-106">In caso di modifica dei dati, il valore hash cambierà in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="67af9-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="67af9-107">Gli hash non sono utili per la crittografia dei dati perché non sono destinati a essere usati per riprodurre i dati originali dal valore hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="67af9-108">Gli hash sono particolarmente utili per verificare l'integrità dei dati quando vengono utilizzati con un algoritmo di firma asimmetrica.</span><span class="sxs-lookup"><span data-stu-id="67af9-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="67af9-109">Se, ad esempio, è stato eseguito l'hashing di un messaggio di testo, la firma dell'hash e il valore hash firmato è stato incluso nel messaggio originale, il destinatario potrebbe verificare l'hash firmato, creare il valore hash per il messaggio ricevuto, quindi confrontare il valore hash con il valore hash firmato incluso nel messaggio originale.</span><span class="sxs-lookup"><span data-stu-id="67af9-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="67af9-110">Se i due valori hash sono identici, il destinatario può essere ragionevolmente sicuro che il messaggio originale non sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="67af9-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="67af9-111">Le dimensioni del valore hash sono fisse per un algoritmo di hash specifico.</span><span class="sxs-lookup"><span data-stu-id="67af9-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="67af9-112">Ciò significa che, indipendentemente dalla dimensione del blocco di dati, il valore hash sarà sempre dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="67af9-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="67af9-113">Ad esempio, l'algoritmo di hash SHA256 ha una dimensione del valore hash di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="67af9-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="67af9-114">Creazione di un oggetto hash</span><span class="sxs-lookup"><span data-stu-id="67af9-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="67af9-115">Creazione di un oggetto di hashing riutilizzabile</span><span class="sxs-lookup"><span data-stu-id="67af9-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="67af9-116">Duplicazione di un oggetto hash</span><span class="sxs-lookup"><span data-stu-id="67af9-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="67af9-117">Creazione di un oggetto hash</span><span class="sxs-lookup"><span data-stu-id="67af9-117">Creating a Hashing Object</span></span>

<span data-ttu-id="67af9-118">Per creare un hash con CNG, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="67af9-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="67af9-119">Aprire un provider di algoritmi che supporta l'algoritmo desiderato.</span><span class="sxs-lookup"><span data-stu-id="67af9-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="67af9-120">Gli algoritmi di hash tipici includono MD2, MD4, MD5, SHA-1 e SHA256.</span><span class="sxs-lookup"><span data-stu-id="67af9-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="67af9-121">Chiamare la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel parametro *pszAlgId* .</span><span class="sxs-lookup"><span data-stu-id="67af9-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="67af9-122">La funzione restituisce un handle per il provider.</span><span class="sxs-lookup"><span data-stu-id="67af9-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="67af9-123">Per creare l'oggetto hash, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="67af9-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="67af9-124">Ottenere le dimensioni dell'oggetto chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la proprietà della **\_ \_ lunghezza dell'oggetto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="67af9-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="67af9-125">Allocare memoria per conservare l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="67af9-126">Creare l'oggetto chiamando la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="67af9-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="67af9-127">Hash dei dati.</span><span class="sxs-lookup"><span data-stu-id="67af9-127">Hash the data.</span></span> <span data-ttu-id="67af9-128">Questa operazione comporta la chiamata della funzione [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) una o più volte.</span><span class="sxs-lookup"><span data-stu-id="67af9-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="67af9-129">Ogni chiamata accoda i dati specificati all'hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="67af9-130">Per ottenere il valore hash, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="67af9-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="67af9-131">Recuperare le dimensioni del valore chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la proprietà **BCRYPT \_ hash \_ length** .</span><span class="sxs-lookup"><span data-stu-id="67af9-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="67af9-132">Allocare memoria per conservare il valore.</span><span class="sxs-lookup"><span data-stu-id="67af9-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="67af9-133">Recuperare il valore hash chiamando la funzione [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) .</span><span class="sxs-lookup"><span data-stu-id="67af9-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="67af9-134">Dopo che questa funzione è stata chiamata, l'oggetto hash non è più valido.</span><span class="sxs-lookup"><span data-stu-id="67af9-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="67af9-135">Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:</span><span class="sxs-lookup"><span data-stu-id="67af9-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="67af9-136">Chiudere l'oggetto hash passando l'handle hash alla funzione [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="67af9-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="67af9-137">Liberare la memoria allocata per l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="67af9-138">Se non si intende creare altri oggetti hash, chiudere il provider dell'algoritmo passando l'handle del provider alla funzione [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="67af9-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="67af9-139">Se si creano più oggetti hash, è consigliabile riutilizzare il provider dell'algoritmo anziché creare ed eliminare più volte lo stesso tipo di provider di algoritmi.</span><span class="sxs-lookup"><span data-stu-id="67af9-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="67af9-140">Al termine dell'utilizzo della memoria per il valore hash, liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="67af9-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="67af9-141">Nell'esempio seguente viene illustrato come creare un valore hash utilizzando CNG.</span><span class="sxs-lookup"><span data-stu-id="67af9-141">The following example shows how to create a hash value by using CNG.</span></span>


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



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="67af9-142">Creazione di un oggetto di hashing riutilizzabile</span><span class="sxs-lookup"><span data-stu-id="67af9-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="67af9-143">A partire da Windows 8 e Windows Server 2012, è possibile creare un oggetto hash riutilizzabile per gli scenari in cui è necessario calcolare più hash o HMAC in rapida successione.</span><span class="sxs-lookup"><span data-stu-id="67af9-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="67af9-144">A tale scopo, specificare **il \_ \_ \_ flag BCRYPT hash riutilizzabile** quando si chiama la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="67af9-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="67af9-145">Tutti i provider di algoritmi hash Microsoft supportano questo flag.</span><span class="sxs-lookup"><span data-stu-id="67af9-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="67af9-146">Un oggetto hash creato mediante questo flag può essere riutilizzato immediatamente dopo la chiamata a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) come se fosse stato appena creato chiamando [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="67af9-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="67af9-147">Per creare un oggetto hash riutilizzabile, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="67af9-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="67af9-148">Aprire un provider di algoritmi che supporta l'algoritmo di hashing desiderato.</span><span class="sxs-lookup"><span data-stu-id="67af9-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="67af9-149">Chiamare la funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) e specificare l'identificatore dell'algoritmo appropriato nel parametro *pszAlgId* e **nel \_ \_ \_ flag BCRYPT hash riutilizzabile** nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="67af9-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="67af9-150">La funzione restituisce un handle per il provider.</span><span class="sxs-lookup"><span data-stu-id="67af9-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="67af9-151">Per creare l'oggetto hash, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="67af9-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="67af9-152">Ottenere le dimensioni dell'oggetto chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per recuperare la proprietà della **\_ \_ lunghezza dell'oggetto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="67af9-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="67af9-153">Allocare memoria per conservare l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="67af9-154">Creare l'oggetto chiamando la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="67af9-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="67af9-155">Specificare **il \_ \_ \_ flag BCRYPT hash riutilizzabile** nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="67af9-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="67af9-156">Hash dei dati chiamando la funzione [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="67af9-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="67af9-157">Per ottenere il valore hash, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="67af9-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="67af9-158">Ottenere la dimensione del valore hash chiamando la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere la proprietà **BCRYPT \_ hash \_ length** .</span><span class="sxs-lookup"><span data-stu-id="67af9-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="67af9-159">Allocare memoria per conservare il valore.</span><span class="sxs-lookup"><span data-stu-id="67af9-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="67af9-160">Ottenere il valore hash chiamando [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span><span class="sxs-lookup"><span data-stu-id="67af9-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="67af9-161">Per riutilizzare l'oggetto hash con nuovi dati, andare al passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="67af9-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="67af9-162">Per completare questa procedura, è necessario eseguire i passaggi di pulizia seguenti:</span><span class="sxs-lookup"><span data-stu-id="67af9-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="67af9-163">Chiudere l'oggetto hash passando l'handle hash alla funzione [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="67af9-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="67af9-164">Liberare la memoria allocata per l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="67af9-165">Se non si intende creare altri oggetti hash, chiudere il provider dell'algoritmo passando l'handle del provider alla funzione [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="67af9-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="67af9-166">Al termine dell'utilizzo della memoria per il valore hash, liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="67af9-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="67af9-167">Duplicazione di un oggetto hash</span><span class="sxs-lookup"><span data-stu-id="67af9-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="67af9-168">In alcuni casi può essere utile eseguire l'hashing di una quantità di dati comuni e quindi creare due oggetti hash distinti dai dati comuni.</span><span class="sxs-lookup"><span data-stu-id="67af9-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="67af9-169">Per eseguire questa operazione, non è necessario creare due oggetti hash distinti ed eseguire l'hashing dei dati comuni due volte.</span><span class="sxs-lookup"><span data-stu-id="67af9-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="67af9-170">È possibile creare un singolo oggetto hash e aggiungere tutti i dati comuni all'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="67af9-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="67af9-171">Quindi, è possibile usare la funzione [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) per creare un duplicato dell'oggetto hash originale.</span><span class="sxs-lookup"><span data-stu-id="67af9-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="67af9-172">L'oggetto hash duplicato contiene tutte le stesse informazioni sullo stato e i dati con hash dell'originale, ma si tratta di un oggetto hash completamente indipendente.</span><span class="sxs-lookup"><span data-stu-id="67af9-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="67af9-173">È ora possibile aggiungere i dati univoci a ognuno degli oggetti hash e ottenere il valore hash come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="67af9-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="67af9-174">Questa tecnica è utile quando si esegue l'hashing di una quantità probabilmente elevata di dati comuni.</span><span class="sxs-lookup"><span data-stu-id="67af9-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="67af9-175">È necessario solo aggiungere i dati comuni all'hash originale una volta, quindi è possibile duplicare l'oggetto hash per ottenere un oggetto hash univoco.</span><span class="sxs-lookup"><span data-stu-id="67af9-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 

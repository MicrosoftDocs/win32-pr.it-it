---
description: Fornisce funzioni per enumerare e ottenere informazioni sui provider registrati.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Uso delle funzionalità di configurazione della crittografia di CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307227"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="8c94f-103">Uso delle funzionalità di configurazione della crittografia di CNG</span><span class="sxs-lookup"><span data-stu-id="8c94f-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="8c94f-104">L'API CNG fornisce funzioni per enumerare e ottenere informazioni sui provider registrati.</span><span class="sxs-lookup"><span data-stu-id="8c94f-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="8c94f-105">Enumerazione dei provider</span><span class="sxs-lookup"><span data-stu-id="8c94f-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="8c94f-106">Recupero delle informazioni di registrazione del provider</span><span class="sxs-lookup"><span data-stu-id="8c94f-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="8c94f-107">Enumerazione dei provider</span><span class="sxs-lookup"><span data-stu-id="8c94f-107">Enumerating Providers</span></span>

<span data-ttu-id="8c94f-108">Utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per enumerare i provider registrati.</span><span class="sxs-lookup"><span data-stu-id="8c94f-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="8c94f-109">La funzione **BCryptEnumRegisteredProviders** può essere chiamata in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c94f-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="8c94f-110">Il primo consiste nell'allocazione della memoria da parte della funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) .</span><span class="sxs-lookup"><span data-stu-id="8c94f-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="8c94f-111">Questa operazione viene eseguita passando l'indirizzo di un puntatore **null** per il parametro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8c94f-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="8c94f-112">Tramite questo codice verrà allocata la memoria necessaria per la struttura dei [**\_ provider di crittografia**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e le stringhe associate.</span><span class="sxs-lookup"><span data-stu-id="8c94f-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="8c94f-113">Quando la funzione **BCryptEnumRegisteredProviders** viene usata in questo modo, è necessario liberare la memoria quando non è più necessaria passando *PpBuffer* alla funzione [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .</span><span class="sxs-lookup"><span data-stu-id="8c94f-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="8c94f-114">Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="8c94f-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  <span data-ttu-id="8c94f-115">Il secondo metodo consiste nell'allocare la memoria necessaria.</span><span class="sxs-lookup"><span data-stu-id="8c94f-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="8c94f-116">Questa operazione viene eseguita chiamando la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) con **null** per il parametro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8c94f-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="8c94f-117">La funzione **BCryptEnumRegisteredProviders** viene posizionata nel valore a cui punta il parametro *pcbBuffer* , ovvero la dimensione richiesta, in byte, della struttura dei [**\_ provider di crittografia**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e di tutte le stringhe.</span><span class="sxs-lookup"><span data-stu-id="8c94f-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="8c94f-118">Si alloca quindi la memoria necessaria e si passa l'indirizzo del puntatore del buffer per il parametro *ppBuffer* in una seconda chiamata alla funzione **BCryptEnumRegisteredProviders** .</span><span class="sxs-lookup"><span data-stu-id="8c94f-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="8c94f-119">Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per allocare e utilizzare il proprio buffer.</span><span class="sxs-lookup"><span data-stu-id="8c94f-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="8c94f-120">Recupero delle informazioni di registrazione del provider</span><span class="sxs-lookup"><span data-stu-id="8c94f-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="8c94f-121">La funzione [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) viene utilizzata per ottenere informazioni aggiuntive specifiche per la registrazione relative a un provider.</span><span class="sxs-lookup"><span data-stu-id="8c94f-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="8c94f-122">Questa funzione accetta il nome del provider per il quale si desidera ottenere informazioni, la modalità del provider desiderata (modalità kernel, modalità utente o entrambi) e l'identificatore dell'interfaccia del provider per il quale recuperare le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="8c94f-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="8c94f-123">Ad esempio, per ottenere le informazioni di registrazione della modalità utente per l'interfaccia di crittografia per il provider "Microsoft primitive provider", effettuare una chiamata simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="8c94f-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="8c94f-124">Come la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la funzione [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) può allocare memoria per l'utente oppure è possibile allocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="8c94f-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="8c94f-125">Il processo è lo stesso per le due funzioni.</span><span class="sxs-lookup"><span data-stu-id="8c94f-125">The process is the same for the two functions.</span></span>

 

 




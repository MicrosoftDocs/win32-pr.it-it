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
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Uso delle funzionalità di configurazione della crittografia di CNG

L'API CNG fornisce funzioni per enumerare e ottenere informazioni sui provider registrati.

-   [Enumerazione dei provider](#enumerating-providers)
-   [Recupero delle informazioni di registrazione del provider](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Enumerazione dei provider

Utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per enumerare i provider registrati. La funzione **BCryptEnumRegisteredProviders** può essere chiamata in uno dei due modi seguenti:

1.  Il primo consiste nell'allocazione della memoria da parte della funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) . Questa operazione viene eseguita passando l'indirizzo di un puntatore **null** per il parametro *ppBuffer* . Tramite questo codice verrà allocata la memoria necessaria per la struttura dei [**\_ provider di crittografia**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e le stringhe associate. Quando la funzione **BCryptEnumRegisteredProviders** viene usata in questo modo, è necessario liberare la memoria quando non è più necessaria passando *PpBuffer* alla funzione [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .

    Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per allocare il buffer.

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

    

2.  Il secondo metodo consiste nell'allocare la memoria necessaria. Questa operazione viene eseguita chiamando la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) con **null** per il parametro *ppBuffer* . La funzione **BCryptEnumRegisteredProviders** viene posizionata nel valore a cui punta il parametro *pcbBuffer* , ovvero la dimensione richiesta, in byte, della struttura dei [**\_ provider di crittografia**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) e di tutte le stringhe. Si alloca quindi la memoria necessaria e si passa l'indirizzo del puntatore del buffer per il parametro *ppBuffer* in una seconda chiamata alla funzione **BCryptEnumRegisteredProviders** .

    Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) per allocare e utilizzare il proprio buffer.

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

    

## <a name="getting-provider-registration-information"></a>Recupero delle informazioni di registrazione del provider

La funzione [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) viene utilizzata per ottenere informazioni aggiuntive specifiche per la registrazione relative a un provider. Questa funzione accetta il nome del provider per il quale si desidera ottenere informazioni, la modalità del provider desiderata (modalità kernel, modalità utente o entrambi) e l'identificatore dell'interfaccia del provider per il quale recuperare le informazioni di registrazione. Ad esempio, per ottenere le informazioni di registrazione della modalità utente per l'interfaccia di crittografia per il provider "Microsoft primitive provider", effettuare una chiamata simile alla seguente.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Come la funzione [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la funzione [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) può allocare memoria per l'utente oppure è possibile allocare la memoria. Il processo è lo stesso per le due funzioni.

 

 




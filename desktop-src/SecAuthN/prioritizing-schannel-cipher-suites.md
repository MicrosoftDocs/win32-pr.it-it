---
description: "L'API CNG (Cryptography API: Next Generation) fornisce funzioni che ese forniscono funzioni per l'esecuzione di query, l'aggiunta, la rimozione e l'assegnazione di priorità ai pacchetti di crittografia supportati da un provider. Le modifiche apportate tramite queste funzioni vengono applicate immediatamente e non richiedono il riavvio di un server attivo."
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Assegnazione delle priorità ai pacchetti di crittografia Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920770"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Assegnazione delle priorità ai pacchetti di crittografia Schannel

[L'API CNG (Cryptography API: Next Generation)](../seccng/cng-portal.md) fornisce funzioni che ese forniscono funzioni per l'esecuzione di query, l'aggiunta, la rimozione e l'assegnazione di priorità ai pacchetti di crittografia supportati da un provider. Le modifiche apportate tramite queste funzioni vengono applicate immediatamente e non richiedono il riavvio di un server attivo.

> [!Note]
> È anche possibile modificare l'elenco dei pacchetti di crittografia configurando le impostazioni dei criteri di gruppo **SSL Cipher Suite Order** usando lo snap-in Criteri di gruppo Object Microsoft Management Console.
> 
> **Per configurare **l'impostazione di Criteri** di gruppo SSL Cipher Suite Order**
> 
> 1.  Al prompt dei comandi immettere **gpedit.msc**. Verrà **Editor oggetti Criteri di gruppo** la finestra di dialogo.
> 2.  Espandere **Configurazione computer**, **Modelli amministrativi**, **Rete**, quindi fare clic su Configurazione **SSL Impostazioni**.
> 3.  In Ssl Configuration Impostazioni (Configurazione **SSL)** fare clic **sull'impostazione SSL Cipher Suite Order (Ordine della suite di crittografia SSL).**
> 4.  Nel riquadro **SSL Cipher Suite Order (Ordine della suite** di crittografia SSL) scorrere fino alla parte inferiore del riquadro.
> 5.  Seguire le istruzioni con **l'etichetta Come modificare questa impostazione.**
> 
> È necessario riavviare il computer dopo aver modificato questa impostazione per l'applicazione delle modifiche.

 

L'elenco dei pacchetti di crittografia è limitato a 1023 caratteri.

Per classificare in ordine di priorità i pacchetti di crittografia Schannel, vedere gli esempi seguenti.

-   [Elenco dei pacchetti di crittografia supportati](#listing-supported-cipher-suites)
-   [Aggiunta, rimozione e assegnazione di priorità ai pacchetti di crittografia](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Elenco dei pacchetti di crittografia supportati

Chiamare la [**funzione BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati da un provider in ordine di priorità.

L'esempio seguente illustra come usare la [**funzione BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Aggiunta, rimozione e assegnazione di priorità ai pacchetti di crittografia

Chiamare le [**funzioni BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) per aggiungere e rimuovere pacchetti di crittografia dall'elenco dei pacchetti di crittografia supportati.

Quando si aggiunge un pacchetto di crittografia, impostare il valore del parametro *dwPosition* della funzione [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) su **CRYPT \_ PRIORITY \_ TOP** per aggiungerlo all'inizio dell'elenco con priorità oppure su **CRYPT \_ PRIORITY \_ BOTTOM** per aggiungerlo alla fine dell'elenco.

Per classificare in ordine di priorità l'elenco dei pacchetti di crittografia, rimuovere tutti i pacchetti di crittografia dall'elenco e quindi aggiungere i pacchetti di crittografia all'elenco nell'ordine desiderato.

L'esempio seguente illustra come aggiungere un pacchetto di crittografia all'inizio dell'elenco con priorità per il provider Microsoft Schannel predefinito.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



L'esempio seguente illustra come rimuovere un pacchetto di crittografia dall'elenco con priorità per il provider Microsoft Schannel predefinito.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 

---
description: 'Cryptography API: Next Generation (CNG) fornisce funzioni che eseguono query, aggiungono, rimuovono e assegnano priorità ai pacchetti di crittografia supportati da un provider. Le modifiche apportate tramite queste funzioni hanno effetto immediato e non richiedono il riavvio di un server attivo.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Assegnazione delle priorità ai pacchetti di crittografia Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234575"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Assegnazione delle priorità ai pacchetti di crittografia Schannel

[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) fornisce funzioni che eseguono query, aggiungono, rimuovono e assegnano priorità ai pacchetti di crittografia supportati da un provider. Le modifiche apportate tramite queste funzioni hanno effetto immediato e non richiedono il riavvio di un server attivo.

> [!Note]
> È anche possibile modificare l'elenco di pacchetti di crittografia configurando le impostazioni di criteri di gruppo per l'ordine dei pacchetti di **crittografia SSL** tramite lo snap-in oggetto Criteri di gruppo in Microsoft Management Console.
> 
> **Per configurare l'impostazione di criteri di gruppo **per l'ordine del pacchetto di crittografia SSL****
> 
> 1.  Al prompt dei comandi, immettere **gpedit. msc**. Viene visualizzato il **Editor oggetti Criteri di gruppo** .
> 2.  Espandere **Configurazione computer**, **modelli amministrativi**, **rete**, quindi fare clic su **impostazioni di configurazione SSL**.
> 3.  In **impostazioni di configurazione SSL** fare clic sull'impostazione dell' **ordine del pacchetto di crittografia SSL** .
> 4.  Nel riquadro dell' **ordine del pacchetto di crittografia SSL** scorrere fino alla fine del riquadro.
> 5.  Seguire le istruzioni riportate nell'etichetta **come modificare questa impostazione**.
> 
> Per rendere effettive le modifiche, è necessario riavviare il computer dopo aver modificato questa impostazione.

 

L'elenco dei pacchetti di crittografia è limitato a 1023 caratteri.

Per definire la priorità dei pacchetti di crittografia Schannel, vedere gli esempi seguenti.

-   [Elenco di pacchetti di crittografia supportati](#listing-supported-cipher-suites)
-   [Aggiunta, rimozione e assegnazione di priorità ai pacchetti di crittografia](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Elenco di pacchetti di crittografia supportati

Chiamare la funzione [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati da un provider in ordine di priorità.

Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati.


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

Chiamare le funzioni [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) per aggiungere e rimuovere i pacchetti di crittografia dall'elenco dei pacchetti di crittografia supportati.

Quando si aggiunge un pacchetto di crittografia, impostare il valore del parametro *dwPosition* della funzione [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) su **crypt \_ Priority \_ Top** per aggiungerlo all'inizio dell'elenco in ordine di priorità o per **crittografare la priorità in \_ \_ basso** per aggiungerlo alla fine dell'elenco.

Per classificare in ordine di priorità l'elenco dei pacchetti di crittografia, rimuovere tutti i pacchetti di crittografia dall'elenco e quindi aggiungere i pacchetti di crittografia all'elenco nell'ordine desiderato.

Nell'esempio seguente viene illustrato come aggiungere un pacchetto di crittografia all'inizio dell'elenco con priorità per il provider Microsoft Schannel predefinito.


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



Nell'esempio seguente viene illustrato come rimuovere un pacchetto di crittografia dall'elenco con priorità per il provider Microsoft Schannel predefinito.


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



 

 

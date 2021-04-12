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
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="962c6-104">Assegnazione delle priorità ai pacchetti di crittografia Schannel</span><span class="sxs-lookup"><span data-stu-id="962c6-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="962c6-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) fornisce funzioni che eseguono query, aggiungono, rimuovono e assegnano priorità ai pacchetti di crittografia supportati da un provider.</span><span class="sxs-lookup"><span data-stu-id="962c6-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="962c6-106">Le modifiche apportate tramite queste funzioni hanno effetto immediato e non richiedono il riavvio di un server attivo.</span><span class="sxs-lookup"><span data-stu-id="962c6-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="962c6-107">È anche possibile modificare l'elenco di pacchetti di crittografia configurando le impostazioni di criteri di gruppo per l'ordine dei pacchetti di **crittografia SSL** tramite lo snap-in oggetto Criteri di gruppo in Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="962c6-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="962c6-108">\*\*Per configurare l'impostazione di criteri di gruppo \*\*per l'ordine del pacchetto di crittografia SSL\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="962c6-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="962c6-109">Al prompt dei comandi, immettere **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="962c6-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="962c6-110">Viene visualizzato il **Editor oggetti Criteri di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="962c6-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="962c6-111">Espandere **Configurazione computer**, **modelli amministrativi**, **rete**, quindi fare clic su **impostazioni di configurazione SSL**.</span><span class="sxs-lookup"><span data-stu-id="962c6-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="962c6-112">In **impostazioni di configurazione SSL** fare clic sull'impostazione dell' **ordine del pacchetto di crittografia SSL** .</span><span class="sxs-lookup"><span data-stu-id="962c6-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="962c6-113">Nel riquadro dell' **ordine del pacchetto di crittografia SSL** scorrere fino alla fine del riquadro.</span><span class="sxs-lookup"><span data-stu-id="962c6-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="962c6-114">Seguire le istruzioni riportate nell'etichetta **come modificare questa impostazione**.</span><span class="sxs-lookup"><span data-stu-id="962c6-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="962c6-115">Per rendere effettive le modifiche, è necessario riavviare il computer dopo aver modificato questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="962c6-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="962c6-116">L'elenco dei pacchetti di crittografia è limitato a 1023 caratteri.</span><span class="sxs-lookup"><span data-stu-id="962c6-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="962c6-117">Per definire la priorità dei pacchetti di crittografia Schannel, vedere gli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="962c6-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="962c6-118">Elenco di pacchetti di crittografia supportati</span><span class="sxs-lookup"><span data-stu-id="962c6-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="962c6-119">Aggiunta, rimozione e assegnazione di priorità ai pacchetti di crittografia</span><span class="sxs-lookup"><span data-stu-id="962c6-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="962c6-120">Elenco di pacchetti di crittografia supportati</span><span class="sxs-lookup"><span data-stu-id="962c6-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="962c6-121">Chiamare la funzione [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati da un provider in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="962c6-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="962c6-122">Nell'esempio seguente viene illustrato come utilizzare la funzione [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) per elencare i pacchetti di crittografia supportati.</span><span class="sxs-lookup"><span data-stu-id="962c6-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="962c6-123">Aggiunta, rimozione e assegnazione di priorità ai pacchetti di crittografia</span><span class="sxs-lookup"><span data-stu-id="962c6-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="962c6-124">Chiamare le funzioni [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) e [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) per aggiungere e rimuovere i pacchetti di crittografia dall'elenco dei pacchetti di crittografia supportati.</span><span class="sxs-lookup"><span data-stu-id="962c6-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="962c6-125">Quando si aggiunge un pacchetto di crittografia, impostare il valore del parametro *dwPosition* della funzione [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) su **crypt \_ Priority \_ Top** per aggiungerlo all'inizio dell'elenco in ordine di priorità o per **crittografare la priorità in \_ \_ basso** per aggiungerlo alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="962c6-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="962c6-126">Per classificare in ordine di priorità l'elenco dei pacchetti di crittografia, rimuovere tutti i pacchetti di crittografia dall'elenco e quindi aggiungere i pacchetti di crittografia all'elenco nell'ordine desiderato.</span><span class="sxs-lookup"><span data-stu-id="962c6-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="962c6-127">Nell'esempio seguente viene illustrato come aggiungere un pacchetto di crittografia all'inizio dell'elenco con priorità per il provider Microsoft Schannel predefinito.</span><span class="sxs-lookup"><span data-stu-id="962c6-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



<span data-ttu-id="962c6-128">Nell'esempio seguente viene illustrato come rimuovere un pacchetto di crittografia dall'elenco con priorità per il provider Microsoft Schannel predefinito.</span><span class="sxs-lookup"><span data-stu-id="962c6-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



 

 

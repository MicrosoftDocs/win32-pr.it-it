---
description: Nell'esempio seguente viene crittografato e decrittografato un BLOB di dati tramite CryptProtectData e CryptUnprotectData.
ms.assetid: 51607aad-9fa8-4db6-bd2a-3821dce619e7
title: 'Esempio di programma C: uso di CryptProtectData'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87359bf6e4d90c4e46140aa9e114ffabf0a5ad80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885066"
---
# <a name="example-c-program-using-cryptprotectdata"></a><span data-ttu-id="f7455-103">Esempio di programma C: uso di CryptProtectData</span><span class="sxs-lookup"><span data-stu-id="f7455-103">Example C Program: Using CryptProtectData</span></span>

<span data-ttu-id="f7455-104">Nell'esempio seguente viene crittografato e decrittografato un [*BLOB*](../secgloss/b-gly.md) di dati tramite [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="f7455-104">The following example encrypts and decrypts a data [*BLOB*](../secgloss/b-gly.md) using [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata).</span></span>

<span data-ttu-id="f7455-105">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7455-105">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="f7455-106">Inizializzazione di una struttura di dati [**CRYPTPROTECT \_ PROMPTSTRUCT**](/windows/desktop/api/Dpapi/ns-dpapi-cryptprotect_promptstruct) .</span><span class="sxs-lookup"><span data-stu-id="f7455-106">Initializing a [**CRYPTPROTECT\_PROMPTSTRUCT**](/windows/desktop/api/Dpapi/ns-dpapi-cryptprotect_promptstruct) data structure.</span></span>
-   <span data-ttu-id="f7455-107">Uso di [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) per crittografare un BLOB di dati.</span><span class="sxs-lookup"><span data-stu-id="f7455-107">Using [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to encrypt a data BLOB.</span></span>
-   <span data-ttu-id="f7455-108">Utilizzo di [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata) per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="f7455-108">Using [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata) to decrypt the data.</span></span>
-   <span data-ttu-id="f7455-109">Utilizzo di [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) per rilasciare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="f7455-109">Using [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release allocated memory.</span></span>

<span data-ttu-id="f7455-110">In questo esempio viene utilizzata la funzione [**MyHandleError**](myhandleerror.md) .</span><span class="sxs-lookup"><span data-stu-id="f7455-110">This example uses the [**MyHandleError**](myhandleerror.md) function.</span></span> <span data-ttu-id="f7455-111">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f7455-111">The code for this function is included with the sample.</span></span> <span data-ttu-id="f7455-112">Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f7455-112">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="f7455-113">Nell'esempio seguente viene illustrata la protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f7455-113">The following example shows protecting data.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{

// Copyright (C) Microsoft.  All rights reserved.
// Encrypt data from DATA_BLOB DataIn to DATA_BLOB DataOut.
// Then decrypt to DATA_BLOB DataVerify.

//-------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataIn;
DATA_BLOB DataOut;
DATA_BLOB DataVerify;
BYTE *pbDataInput =(BYTE *)"Hello world of data protection.";
DWORD cbDataInput = strlen((char *)pbDataInput)+1;
DataIn.pbData = pbDataInput;    
DataIn.cbData = cbDataInput;
CRYPTPROTECT_PROMPTSTRUCT PromptStruct;
LPWSTR pDescrOut = NULL;

//-------------------------------------------------------------------
//  Begin processing.

printf("The data to be encrypted is: %s\n",pbDataInput);

//-------------------------------------------------------------------
//  Initialize PromptStruct.

ZeroMemory(&PromptStruct, sizeof(PromptStruct));
PromptStruct.cbSize = sizeof(PromptStruct);
PromptStruct.dwPromptFlags = CRYPTPROTECT_PROMPT_ON_PROTECT;
PromptStruct.szPrompt = L"This is a user prompt.";

//-------------------------------------------------------------------
//  Begin protect phase.

if(CryptProtectData(
     &DataIn,
     L"This is the description string.", // A description string. 
     NULL,                               // Optional entropy
                                         // not used.
     NULL,                               // Reserved.
     &PromptStruct,                      // Pass a PromptStruct.
     0,
     &DataOut))
{
     printf("The encryption phase worked. \n");
}
else
{
    MyHandleError("Encryption error!");
}
//-------------------------------------------------------------------
//   Begin unprotect phase.

if (CryptUnprotectData(
        &DataOut,
        &pDescrOut,
        NULL,                 // Optional entropy
        NULL,                 // Reserved
        &PromptStruct,        // Optional PromptStruct
        0,
        &DataVerify))
{
     printf("The decrypted data is: %s\n", DataVerify.pbData);
     printf("The description of the data was: %S\n",pDescrOut);
}
else
{
    MyHandleError("Decryption error!");
}
//-------------------------------------------------------------------
// At this point, memcmp could be used to compare DataIn.pbData and 
// DataVerify.pbDate for equality. If the two functions worked
// correctly, the two byte strings are identical. 

//-------------------------------------------------------------------
//  Clean up.

LocalFree(pDescrOut);
LocalFree(DataOut.pbData);
LocalFree(DataVerify.pbData);
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the  
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 

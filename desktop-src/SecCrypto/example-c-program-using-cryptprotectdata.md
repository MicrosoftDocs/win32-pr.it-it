---
description: L'esempio seguente crittografa e decrittografa un BLOB di dati usando CryptProtectData e CryptUnprotectData.
ms.assetid: 51607aad-9fa8-4db6-bd2a-3821dce619e7
title: 'Esempio di programma C: uso di CryptProtectData'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6639bc3f0dbabc3b82c41aaa858d9ad1c8a5b9e7b10661a3a53f7b1730baad40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140772"
---
# <a name="example-c-program-using-cryptprotectdata"></a>Esempio di programma C: uso di CryptProtectData

L'esempio seguente crittografa e decrittografa un [*BLOB*](../secgloss/b-gly.md) di dati [**usando CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata).

Questo esempio illustra le attività seguenti e le funzioni CryptoAPI:

-   Inizializzazione di una [**struttura di dati CRYPTPROTECT \_ PROMPTSTRUCT.**](/windows/desktop/api/Dpapi/ns-dpapi-cryptprotect_promptstruct)
-   Uso [**di CryptProtectData per**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) crittografare un BLOB di dati.
-   Uso [**di CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata) per decrittografare i dati.
-   Uso [**di LocalFree per rilasciare**](/windows/win32/api/winbase/nf-winbase-localfree) la memoria allocata.

In questo esempio viene utilizzata [**la funzione MyHandleError.**](myhandleerror.md) Il codice per questa funzione è incluso nell'esempio. Il codice per questa e altre funzioni ausiliarie è elencato anche in [per utilizzo generico funzioni](general-purpose-functions.md).

Nell'esempio seguente viene illustrata la protezione dei dati.


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



 

 

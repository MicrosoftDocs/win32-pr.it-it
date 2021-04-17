---
description: Nell'esempio seguente viene illustrata la creazione di una chiave crittografica della sessione dall'hash di una password, nonché l'utilizzo della funzione CryptDeriveKey e delle funzioni correlate.
ms.assetid: f4748725-2a47-487c-b18c-7b27112d1090
title: 'Esempio di programma C: derivazione di una chiave della sessione da una password'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46884fa40a3a5682ca21229048004314bf03609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233504"
---
# <a name="example-c-program-deriving-a-session-key-from-a-password"></a><span data-ttu-id="38193-103">Esempio di programma C: derivazione di una chiave della sessione da una password</span><span class="sxs-lookup"><span data-stu-id="38193-103">Example C Program: Deriving a Session Key from a Password</span></span>

<span data-ttu-id="38193-104">Nell'esempio seguente viene illustrata la creazione di una [*chiave crittografica della sessione*](../secgloss/s-gly.md) dall' [*hash*](../secgloss/h-gly.md) di una password, nonché l'utilizzo della funzione [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) e delle funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="38193-104">The following example demonstrates creating a [*session cryptographic key*](../secgloss/s-gly.md) from the [*hash*](../secgloss/h-gly.md) of a password as well as the use of the function [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) and related functions.</span></span>

<span data-ttu-id="38193-105">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="38193-105">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="38193-106">Chiamata di [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) per acquisire un handle per il CSP predefinito e il [*contenitore di chiavi*](../secgloss/k-gly.md)predefinito.</span><span class="sxs-lookup"><span data-stu-id="38193-106">Calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) to acquiring a handle for the default CSP and the default [*key container*](../secgloss/k-gly.md).</span></span>
-   <span data-ttu-id="38193-107">Utilizzo di [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) per creare un oggetto hash vuoto.</span><span class="sxs-lookup"><span data-stu-id="38193-107">Using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) to create an empty hash object.</span></span>
-   <span data-ttu-id="38193-108">Hashing del testo di una password con [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span><span class="sxs-lookup"><span data-stu-id="38193-108">Hashing the text of a password using [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).</span></span>
-   <span data-ttu-id="38193-109">Derivare una chiave della sessione dalla password con hash usando [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span><span class="sxs-lookup"><span data-stu-id="38193-109">Deriving a session key from the hashed password using [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>
-   <span data-ttu-id="38193-110">Eliminazione definitiva dell'hash e della password.</span><span class="sxs-lookup"><span data-stu-id="38193-110">Destroying the hash and the password.</span></span>
-   <span data-ttu-id="38193-111">Uso di [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) per rilasciare il CSP.</span><span class="sxs-lookup"><span data-stu-id="38193-111">Using [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) to release the CSP.</span></span>

<span data-ttu-id="38193-112">In questo esempio viene usata la funzione [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="38193-112">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="38193-113">Il codice per questa funzione è incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="38193-113">Code for this function is included with the sample.</span></span>

<span data-ttu-id="38193-114">Il codice per questa e altre funzioni ausiliarie è elencato anche in [funzioni per utilizzo generico](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="38193-114">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void GetConsoleInput(char*, UINT);
#define PASSWORD_LENGTH 512

void main()
{
    //----------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.

    HCRYPTPROV hCryptProv;
    HCRYPTKEY hKey;
    HCRYPTHASH hHash;
    CHAR szPassword[PASSWORD_LENGTH] = "";
    DWORD dwLength;

    //----------------------------------------------------------------
    // Get the password from the user.

    fprintf(stderr,"Enter a password to be used to create a key:");

    // Get a password while printing only asterisks to the screen.
    GetConsoleInput(szPassword, PASSWORD_LENGTH);
    printf("The password has been stored.\n");
    dwLength = (DWORD) strlen(szPassword);

    //----------------------------------------------------------------
    // Acquire a cryptographic provider context handle.

    if(CryptAcquireContext(
       &hCryptProv,
       NULL,
       NULL,
       PROV_RSA_FULL,
       0))
    {
        printf("A context has been acquired. \n");
    }
    else
    {
         MyHandleError("Error during CryptAcquireContext!");
    }
    //----------------------------------------------------------------
    // Create an empty hash object.

    if(CryptCreateHash(
       hCryptProv,
       CALG_MD5,
       0,
       0,
       &hHash))
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptCreateHash!");
    }
    //----------------------------------------------------------------
    // Hash the password string.

    if(CryptHashData(
       hHash,
       (BYTE *)szPassword,
       dwLength,
       0))
    {
         printf("The password has been hashed. \n");
    }
    else
    {
         MyHandleError("Error during CryptHashData!");
    }
    //----------------------------------------------------------------
    // Create a session key based on the hash of the password.

    if(CryptDeriveKey(
       hCryptProv,
       CALG_RC2,
       hHash,
       CRYPT_EXPORTABLE,
       &hKey))
    {
        printf("The key has been derived. \n");
    }
    else
    {
        MyHandleError("Error during CryptDeriveKey!");
    }
    //----------------------------------------------------------------
    // Use hKey as appropriate to encrypt or decrypt a message.

    //----------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
       if(!(CryptDestroyHash(hHash)))
           MyHandleError("Error during CryptDestroyHash");
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
            MyHandleError("Error during CryptDestroyKey");
    }

    // Release the provider handle.
    if(hCryptProv)
    {
       if(!(CryptReleaseContext(hCryptProv, 0)))
           MyHandleError("Error during CryptReleaseContext");
    }
    printf("The program to derive a key completed without error. \n");
} // end main

//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}

//--------------------------------------------------------------------
// The GetConsoleInput function gets an array of characters from the
// keyboard, while printing only asterisks to the screen.

void GetConsoleInput(char* strInput,
                    UINT  intMaxChars)
{
    char ch;
    char minChar = ' ';
    minChar++;

    ch = (char)_getch();
    while (ch != '\r')
    {
        if (ch == '\b' && strlen(strInput) > 0)
        {
            strInput[strlen(strInput)-1]   = '\0';
            printf("\b \b");
        }
        else if ((ch >= minChar) && (strlen(strInput) < intMaxChars))
        {
            strInput[strlen(strInput)+1] = '\0';
            strInput[strlen(strInput)]   = ch;
            _putch('*');
        }
        ch = (char)_getch();
    }
    _putch('\n');
}

```



 

 

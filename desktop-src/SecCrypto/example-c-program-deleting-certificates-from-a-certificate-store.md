---
description: L'esempio seguente elenca i certificati in un archivio certificati di sistema, visualizzando il nome del soggetto di ogni certificato, e consente all'utente di scegliere di eliminare eventuali certificati dall'archivio.
ms.assetid: 52a0287b-7d2a-483e-8bbc-43621c4b7103
title: 'Programma C di esempio: eliminazione di certificati da un archivio certificati'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065a7e0e46f3072d69014e294610ec7ae546d05c98816f809b9b2de92949db62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007855"
---
# <a name="example-c-program-deleting-certificates-from-a-certificate-store"></a>Programma C di esempio: eliminazione di certificati da un archivio certificati

L'esempio seguente elenca i certificati in un archivio certificati di sistema [*,*](../secgloss/c-gly.md)visualizzando il nome del soggetto di ogni certificato e consente all'utente di scegliere di eliminare eventuali certificati dall'archivio. L'esempio ottiene il nome dell'archivio certificati dall'utente e quindi può essere usato per gestire il contenuto di qualsiasi archivio certificati di sistema.

Questo esempio illustra le attività e le [*funzioni CryptoAPI*](../secgloss/c-gly.md) seguenti:

-   Apertura di un archivio certificati di sistema [**tramite CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Elenco dei certificati in un archivio certificati [**tramite CertEnumCertificatesInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)
-   Recupero del nome dell'oggetto di un certificato [**tramite CertGetNameString.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)
-   Confronto tra il nome del soggetto del certificato e il nome dell'autorità emittente del certificato [**tramite CertCompareCertificateName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename).
-   Controllo per determinare se la chiave pubblica del certificato corrente corrisponde alla chiave pubblica di un certificato precedente usando [**CertComparePublicKeyInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo).
-   Duplicazione di un puntatore a [*un contesto di*](../secgloss/c-gly.md) certificato tramite [**CertDuplicateCertificateContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)
-   Confronto dei [**membri CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) di ogni certificato [**tramite CertCompareCertificate.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate)
-   Eliminazione di un certificato da un archivio [**tramite CertDeleteCertificateFromStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   Chiusura di un archivio certificati [**tramite CertCloseStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

Questo esempio ottiene il nome di un archivio certificati di sistema dall'utente, lo apre e passa attraverso i certificati in tale archivio. Per ogni certificato, viene visualizzato il nome del soggetto del certificato e all'utente viene data un'opzione per eliminare il certificato.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HANDLE          hStoreHandle;
PCCERT_CONTEXT  pCertContext=NULL;   
PCCERT_CONTEXT  pDupCertContext; 
PCERT_PUBLIC_KEY_INFO pOldPubKey = NULL;
PCERT_PUBLIC_KEY_INFO pNewPubKey; 
char pszStoreName[256];
char pszNameString[256];
char fResponse ='n';  
char x;

//-------------------------------------------------------------------
// Get the name of the certificate store to open. 
printf("This program maintains the contents of a certificate\n");
printf("store by allowing you to delete any excess certificates\n");
printf("from a store. \n\n");
printf("Please enter the name of the system store to maintain:");
fgets(pszStoreName, 255, stdin);
if (pszStoreName[strlen(pszStoreName) - 1] =='\n')
   pszStoreName[strlen(pszStoreName) - 1] = '\0';
printf("Certificates will be deleted from "
       "the %s store.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hStoreHandle = CertOpenSystemStore(
     NULL,     
     pszStoreName))
{
     printf("The %s store has been opened. \n", pszStoreName);
}
else
{
     MyHandleError("The store was not opened.");
}
//-------------------------------------------------------------------
// Find the certificates in the system store. 

while(pCertContext= CertEnumCertificatesInStore(
    hStoreHandle,
    pCertContext)) // on the first call to the function,
                   //  this parameter is NULL
                   // on all subsequent
                   //  calls, it is the last pointer returned by 
                   //  the function
{
//-------------------------------------------------------------------
// Get and display the name of the subject of the certificate.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
   printf("\nCertificate for %s \n",pszNameString);
}
else
{
   MyHandleError("CertGetName failed.");
}
//-------------------------------------------------------------------
// Check to determine whether the issuer 
// and the subject are the same.

if(CertCompareCertificateName(
   MY_ENCODING_TYPE,
   &(pCertContext->pCertInfo->Issuer),
   &(pCertContext->pCertInfo->Subject)))
{
     printf("The certificate subject and issuer are the same.\n");
}
else
{
     printf("The certificate subject and issuer "
         "are not the same.\n");
}
//--------------------------------------------------------------------
// Determine whether this certificate's public key matches 
// the public key of the last certificate.

pNewPubKey = &(pCertContext->pCertInfo->SubjectPublicKeyInfo);
if(pOldPubKey)
   if(CertComparePublicKeyInfo(
       MY_ENCODING_TYPE,
       pOldPubKey,
       pNewPubKey))
   {
       printf("The public keys are the same.\n");
   }
   else
   {
       printf("This certificate has a different public key.\n");
   }
//-------------------------------------------------------------------
// Reset the old key.

pOldPubKey = pNewPubKey;

//-------------------------------------------------------------------
// Determine whether this certificate is to be deleted. 

printf("Would you like to delete this certificate? (y/n) ");
fResponse = getchar();
if(fResponse == 'y')
{
   //----------------------------------------------------------------
   // Create a duplicate pointer to the certificate to be 
   // deleted. In this way, the original pointer is not freed 
   // when the certificate is deleted from the store 
   // and the enumeration of the certificates in the store can
   // continue. If the original pointer is used, after the 
   // certificate is deleted, the enumeration loop stops.

   if(pDupCertContext = CertDuplicateCertificateContext(
      pCertContext))
   {
       printf("A duplicate pointer was created. Continue. \n");
   }
   else
   {
        MyHandleError("Duplication of the certificate "
            "pointer failed.");
   }

//-------------------------------------------------------------------
// Compare the pCertInfo members of the two certificates 
// to determine whether they are identical.

if(CertCompareCertificate(
      X509_ASN_ENCODING,
      pDupCertContext->pCertInfo, 
      pCertContext->pCertInfo))
{
     printf("The two certificates are identical. \n");
}
else
{
     printf("The two certificates are not identical. \n");
}
//-------------------------------------------------------------------
// Delete the certificate.
   if(CertDeleteCertificateFromStore(
     pDupCertContext))   
   {
       printf("The certificate has been deleted. Continue. \n");
   }
   else
   {
      printf("The deletion of the certificate failed.\n");
   }
} // end if

//-------------------------------------------------------------------
// Clear the input buffer.

x = getchar();

} // end while

//-------------------------------------------------------------------
// Clean up.

CertCloseStore(
   hStoreHandle,
   0);
printf("The program ran to completion successfully. \n");
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 

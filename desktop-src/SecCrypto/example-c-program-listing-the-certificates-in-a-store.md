---
description: Elenca tutti i certificati in un archivio certificati di sistema e il nome dell'oggetto e tutte le proprietà del contesto del certificato di ognuno di questi certificati.
ms.assetid: 4b5361f5-79b1-4b05-a133-1a394da7d6ee
title: 'Programma C di esempio: elenco dei certificati in un archivio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47545d2a4c5b13df57dc4bae5490123c9423a9127f6f5e6dbe0b3a885651d9f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007599"
---
# <a name="example-c-program-listing-the-certificates-in-a-store"></a>Programma C di esempio: elenco dei certificati in un archivio

Il codice di esempio seguente elenca [](../secgloss/c-gly.md) tutti i certificati in un archivio [](../secgloss/c-gly.md) certificati di sistema e il nome del soggetto e tutte le proprietà del contesto del certificato di ognuno di questi certificati. L'esempio ottiene il nome dell'archivio certificati dall'utente e quindi può essere usato per elencare il contenuto di qualsiasi archivio certificati di sistema. Questo esempio illustra anche l'uso di due nuove funzioni dell'interfaccia utente, una che visualizza un certificato e l'altra interfaccia utente che consente all'utente di selezionare un certificato da un elenco dei certificati in un archivio.

Questo codice di esempio illustra le attività e le [*funzioni CryptoAPI*](../secgloss/c-gly.md) seguenti:

-   Apertura di un archivio di sistema [**tramite CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   In un ciclo, enumerazione di tutti i certificati nell'archivio aperto tramite [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).
-   Visualizzazione di un certificato [**tramite CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext).
-   Recupero del nome del soggetto del certificato tramite [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   In un ciclo, usando [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) per ottenere gli identificatori di proprietà di tutte le proprietà associate al certificato.
-   Uso [**di CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) per ottenere ognuna delle proprietà.
-   Visualizzazione di un elenco di certificati in un archivio e consentire a un utente di selezionarne uno [**usando CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore).
-   Chiusura dell'archivio certificati tramite [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).

In questo esempio viene utilizzata la [**funzione MyHandleError**](myhandleerror.md). Il codice per questa funzione è incluso nell'esempio.

Il codice per questa e altre funzioni ausiliarie è elencato anche in [per utilizzo generico funzioni](general-purpose-functions.md).

Nell'esempio seguente viene illustrata l'enumerazione e la visualizzazione dei certificati in un archivio. Per compilare questo esempio, è necessario configurare il compilatore per l'uso di un set di caratteri a byte multipli.


```C++
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>
#include <cryptuiapi.h>

#include <tchar.h>

#pragma comment (lib, "crypt32.lib")
#pragma comment (lib, "cryptui.lib")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This program lists all of the certificates in a system certificate
// store and all of the property identifier numbers of those 
// certificates. It also demonstrates the use of two
// UI functions. One, CryptUIDlgSelectCertificateFromStore, 
// displays the certificates in a store
// and allows the user to select one of them, 
// The other, CryptUIDlgViewContext,
// displays the contents of a single certificate.

//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE       hCertStore;        
PCCERT_CONTEXT   pCertContext=NULL;      
char pszNameString[256];
char pszStoreName[256];
void*            pvData;
DWORD            cbData;
DWORD            dwPropId = 0; 
            // Zero must be used on the first
            // call to the function. After that,
            // the last returned property identifier is passed.

//-------------------------------------------------------------------
//  Begin processing and Get the name of the system certificate store 
//  to be enumerated. Output here is to stderr so that the program  
//  can be run from the command line and stdout can be redirected  
//  to a file.

fprintf(stderr,"Please enter the store name:");
gets_s(pszStoreName, sizeof(pszStoreName));
fprintf(stderr,"The store name is %s.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hCertStore = CertOpenSystemStore(
     NULL,
     pszStoreName))
{
     fprintf(stderr,"The %s store has been opened. \n", 
          pszStoreName);
}
else
{
// If the store was not opened, exit to an error routine.
     MyHandleError("The store was not opened.");
}

//-------------------------------------------------------------------
// Use CertEnumCertificatesInStore to get the certificates 
// from the open store. pCertContext must be reset to
// NULL to retrieve the first certificate in the store.
 
// pCertContext = NULL;

while(pCertContext= CertEnumCertificatesInStore(
     hCertStore,
     pCertContext))
{
//-------------------------------------------------------------------
// A certificate was retrieved. Continue.
//-------------------------------------------------------------------
//  Display the certificate.

if ( CryptUIDlgViewContext(
  CERT_STORE_CERTIFICATE_CONTEXT,
  pCertContext,
  NULL,
  NULL,
  0,
  NULL))
{
//     printf("OK\n");
}
else
{
    MyHandleError("UI failed.");
}

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
   fprintf(stderr,"CertGetName failed. \n");

//-------------------------------------------------------------------
// Loop to find all of the property identifiers for the specified  
// certificate. The loop continues until 
// CertEnumCertificateContextProperties returns zero.

while(dwPropId = CertEnumCertificateContextProperties(
       pCertContext, // The context whose properties are to be listed.
       dwPropId))    // Number of the last property found.  
                     // This must be zero to find the first 
                     // property identifier.
{
//-------------------------------------------------------------------
// When the loop is executed, a property identifier has been found.
// Print the property number.

   printf("Property # %d found->", dwPropId);

//-------------------------------------------------------------------
// Indicate the kind of property found.

   switch(dwPropId)
   {
     case CERT_FRIENDLY_NAME_PROP_ID:
     {
       printf("Display name: ");
       break;
     }
     case CERT_SIGNATURE_HASH_PROP_ID:
     {
       printf("Signature hash identifier ");
       break;
     }
     case CERT_KEY_PROV_HANDLE_PROP_ID:
     {
       printf("KEY PROVE HANDLE");
       break;
     }
     case CERT_KEY_PROV_INFO_PROP_ID:
     {
       printf("KEY PROV INFO PROP ID ");
       break;
     }
     case CERT_SHA1_HASH_PROP_ID:
     {
        printf("SHA1 HASH identifier");
        break;
     }
     case CERT_MD5_HASH_PROP_ID:
     {
        printf("md5 hash identifier ");
        break;
     }
     case CERT_KEY_CONTEXT_PROP_ID:
     {
        printf("KEY CONTEXT PROP identifier");
        break;
     }
     case CERT_KEY_SPEC_PROP_ID:
     {
        printf("KEY SPEC PROP identifier");
        break;
      }
      case CERT_ENHKEY_USAGE_PROP_ID:
      {
        printf("ENHKEY USAGE PROP identifier");
        break;
      }
      case CERT_NEXT_UPDATE_LOCATION_PROP_ID:
      {
        printf("NEXT UPDATE LOCATION PROP identifier");
        break;
      }
      case CERT_PVK_FILE_PROP_ID:
      {
         printf("PVK FILE PROP identifier ");
         break;
      }
      case CERT_DESCRIPTION_PROP_ID:
      {
        printf("DESCRIPTION PROP identifier ");
        break;
      }
      case CERT_ACCESS_STATE_PROP_ID:
      {
        printf("ACCESS STATE PROP identifier ");
        break;
      }
      case CERT_SMART_CARD_DATA_PROP_ID:
      {
         printf("SMART_CARD DATA PROP identifier ");
         break;
      }
      case CERT_EFS_PROP_ID:
      {
        printf("EFS PROP identifier ");
        break;
      }
      case CERT_FORTEZZA_DATA_PROP_ID:
      {
        printf("FORTEZZA DATA PROP identifier ");
        break;
      }
      case CERT_ARCHIVED_PROP_ID:
      {
        printf("ARCHIVED PROP identifier ");
        break;
      }
      case CERT_KEY_IDENTIFIER_PROP_ID:
      {
        printf("KEY IDENTIFIER PROP identifier ");
        break;
      }
      case CERT_AUTO_ENROLL_PROP_ID:
      {
        printf("AUTO ENROLL identifier. ");
        break;
      }
   } // End switch.

//-------------------------------------------------------------------
// Retrieve information on the property by first getting the 
// property size. 
// For more information, see CertGetCertificateContextProperty.

   if(CertGetCertificateContextProperty(
         pCertContext, 
         dwPropId , 
         NULL, 
         &cbData))
    {
    //  Continue.
    }
    else
    {  
    // If the first call to the function failed,
    // exit to an error routine.
        MyHandleError("Call #1 to GetCertContextProperty failed.");
    }
//-------------------------------------------------------------------
// The call succeeded. Use the size to allocate memory 
// for the property.
   
   if(pvData = (void*)malloc(cbData))
   {
   // Memory is allocated. Continue.
   }
   else
   {
   // If memory allocation failed, exit to an error routine.
      MyHandleError("Memory allocation failed.");
   }
   //----------------------------------------------------------------
   // Allocation succeeded. Retrieve the property data.
   
   if(CertGetCertificateContextProperty(
      pCertContext,
      dwPropId,
      pvData, 
      &cbData))
    {
    // The data has been retrieved. Continue.
    }
    else
    {
    // If an error occurred in the second call, 
    // exit to an error routine.
      MyHandleError("Call #2 failed.");
    }
    //---------------------------------------------------------------
    // Show the results.

   printf("The Property Content is %d \n", pvData);
     
   //----------------------------------------------------------------
   // Free the certificate context property memory.
    
   free(pvData);
  }  // End inner while.
} // End outer while.

//-------------------------------------------------------------------
// Select a new certificate by using the user interface.

if(!(pCertContext = CryptUIDlgSelectCertificateFromStore(
  hCertStore,
  NULL,
  NULL,
  NULL,
  CRYPTUI_SELECT_LOCATION_COLUMN,
  0,
  NULL)))
{
    MyHandleError("Select UI failed." );
}


//-------------------------------------------------------------------
// Clean up.

CertFreeCertificateContext(pCertContext);
CertCloseStore(hCertStore,0);
printf("The function completed successfully. \n");
} // End of main.


void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.
```



 

 

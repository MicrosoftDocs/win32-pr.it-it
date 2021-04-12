---
description: Mostra la registrazione (creazione) e l'apertura di un archivio di sistema, la registrazione di un archivio fisico come membro di un archivio di sistema e l'annullamento della registrazione (eliminazione) di un archivio di sistema.
ms.assetid: 857ab592-68c7-4660-b37d-b165aeee14f4
title: 'Esempio di programma C: registrazione di archivi certificati fisici e di sistema'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708a840767b4e49bd1ba5c70dd5ae63f0f9ab7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346546"
---
# <a name="example-c-program-registering-physical-and-system-certificate-stores"></a><span data-ttu-id="6c21e-103">Esempio di programma C: registrazione di archivi certificati fisici e di sistema</span><span class="sxs-lookup"><span data-stu-id="6c21e-103">Example C Program: Registering Physical and System Certificate Stores</span></span>

<span data-ttu-id="6c21e-104">Gli archivi fisici possono essere costituiti da più o meno membri permanenti di un archivio di sistema.</span><span class="sxs-lookup"><span data-stu-id="6c21e-104">Physical stores may be made more or less permanent members of a system store.</span></span> <span data-ttu-id="6c21e-105">Quando un archivio fisico è membro di un archivio di sistema, le operazioni nell'archivio di sistema, ad esempio la ricerca di un certificato, verranno esaminate in tutti gli archivi fisici registrati come membri dell'archivio di sistema.</span><span class="sxs-lookup"><span data-stu-id="6c21e-105">When a physical store is a member of a system store, operations on the system store such as finding a certificate will look in all of the physical stores that are registered as members of the system store.</span></span> <span data-ttu-id="6c21e-106">Un archivio fisico può essere rimosso dall'appartenenza a un archivio di sistema utilizzando una funzione di annullamento della registrazione.</span><span class="sxs-lookup"><span data-stu-id="6c21e-106">A physical store can be removed from membership in a system store by using an unregister function.</span></span>

<span data-ttu-id="6c21e-107">In questo esempio vengono illustrate le attività e le funzioni CryptoAPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="6c21e-107">This example shows the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="6c21e-108">Registrazione (creazione) di un nuovo archivio di sistema tramite [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore).</span><span class="sxs-lookup"><span data-stu-id="6c21e-108">Registering (creating) a new system store using [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore).</span></span>
-   <span data-ttu-id="6c21e-109">Apertura di un archivio di sistema appena creato tramite [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="6c21e-109">Opening a newly created system store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="6c21e-110">Registrazione di un archivio fisico come membro di un archivio di sistema tramite [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="6c21e-110">Registering a physical store as a member of a system store using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>
-   <span data-ttu-id="6c21e-111">Annullamento della registrazione (eliminazione) di un archivio di sistema tramite [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore).</span><span class="sxs-lookup"><span data-stu-id="6c21e-111">Unregistering (deleting) a system store using [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore).</span></span>

<span data-ttu-id="6c21e-112">Questo esempio illustra anche la creazione e l'eliminazione degli archivi di sistema.</span><span class="sxs-lookup"><span data-stu-id="6c21e-112">This example also demonstrates the creation and deletion of system stores.</span></span>


```C++
// This example uses CertRegisterSystemStore.
#pragma comment(lib, "crypt32.lib")

// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{


// Declare and initialize variables.

HCERTSTORE hSystemStore;
DWORD dwFlags= CERT_SYSTEM_STORE_CURRENT_USER;
LPCWSTR pvSystemName= L"NEWSTORE";  // For this setting of 
                                    // dwFlags, the store name may 
                                    // be prefixed with a user name.
CERT_PHYSICAL_STORE_INFO PhysicalStoreInfo;
BYTE fResponse  = 'n';

if(CertRegisterSystemStore(
    pvSystemName,
    dwFlags,
    NULL,
    NULL))
  printf("System store %S is registered. \n",pvSystemName);
else
  printf("The system store did not register. \n");


// Open the NEWSTORE as a system store.

if(hSystemStore = CertOpenStore(
   CERT_STORE_PROV_SYSTEM,   // the store provider type
   0,                        // the encoding type is not needed
   NULL,                     // use the default HCRYPTPROV
   CERT_SYSTEM_STORE_CURRENT_USER,
                             // set the store location in a registry
                             // location
   pvSystemName ))           // the store name as a Unicode string
{
     printf("The new store has been opened as a system store.\n");
}
else
{
     printf("The new store was not opened as a system store.\n");
}
if(hSystemStore)
{
    if(CertCloseStore(hSystemStore,0))
    {
        printf("The system store has been closed.\n");
    }
    else
    {
        printf("The system store could not be closed.\n");
    }
}
else
{
   printf("The system store did not need to be closed.\n");
}


// Initialize PhysicalStoreInfo.

PhysicalStoreInfo.cbSize=sizeof(CERT_PHYSICAL_STORE_INFO);
PhysicalStoreInfo.pszOpenStoreProvider=(LPSTR)
    CERT_STORE_PROV_FILENAME;
PhysicalStoreInfo.dwFlags=CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG;


// Replace the path below with one that is appropriate for you.

PhysicalStoreInfo.OpenParameters.pbData = 
    (BYTE *) L"C:\\temp\\mystore";
PhysicalStoreInfo.OpenParameters.cbData = 
    (wcslen((LPWSTR) PhysicalStoreInfo.OpenParameters.pbData) + 1) * 
    sizeof(WCHAR);

PhysicalStoreInfo.dwPriority=1;
PhysicalStoreInfo.dwOpenEncodingType=MY_ENCODING_TYPE;


// Register the physical store.

if(CertRegisterPhysicalStore(
      L"NEWSTORE",
      dwFlags,
      L"TESTOR.STO",
      &PhysicalStoreInfo,
      NULL
      ))
{
       printf("Physical store is registered. \n");
}
else
{
       printf("The physical store was not registered.\n");
}  


//  Next, unregister the store.

printf("Would you like to unregister the %S store? (y/n) "
       ,pvSystemName);
scanf_s("%c",&fResponse);

if(fResponse=='y')
{
   if(CertUnregisterSystemStore(
     pvSystemName,
     dwFlags))
   {
      printf("System store %S has been unregistered.\n"
          ,pvSystemName);
   }
   else
   {
      printf("The system store was not unregistered.\n");
   }
}
}  // end main


//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to  
//  the standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end of MyHandleError
```



 

 




---
description: La funzione GetSignerCert passa attraverso (enumera) i certificati in un archivio certificati finché non viene trovato un certificato con una chiave di firma.
ms.assetid: a3279492-a154-418d-ab25-45ec458ad483
title: GetSignerCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beff3e220fc8f0c95992c4a14a3dc8b5f5d19fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968661"
---
# <a name="getsignercert"></a><span data-ttu-id="e4a92-103">GetSignerCert</span><span class="sxs-lookup"><span data-stu-id="e4a92-103">GetSignerCert</span></span>

<span data-ttu-id="e4a92-104">La funzione **GetSignerCert** passa attraverso (enumera) i certificati in un [*archivio certificati*](../secgloss/c-gly.md) finché non viene trovato un certificato con una chiave di firma.</span><span class="sxs-lookup"><span data-stu-id="e4a92-104">The **GetSignerCert** function goes through (enumerates) the certificates in a [*certificate store*](../secgloss/c-gly.md) until a certificate with a signature key is found.</span></span> <span data-ttu-id="e4a92-105">Se viene trovato un certificato, viene restituito un puntatore al certificato.</span><span class="sxs-lookup"><span data-stu-id="e4a92-105">If a certificate is found, a pointer to the certificate is returned.</span></span> <span data-ttu-id="e4a92-106">Questo codice illustra:</span><span class="sxs-lookup"><span data-stu-id="e4a92-106">This code demonstrates:</span></span>

-   <span data-ttu-id="e4a92-107">Ricerca di un certificato con una proprietà Certificate.</span><span class="sxs-lookup"><span data-stu-id="e4a92-107">Finding a certificate with a certificate property.</span></span>
-   <span data-ttu-id="e4a92-108">Verifica della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4a92-108">Checking that property.</span></span>
-   <span data-ttu-id="e4a92-109">Restituzione di un puntatore [**al \_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) in cui è stato trovato l'attributo.</span><span class="sxs-lookup"><span data-stu-id="e4a92-109">Returning a pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) where the attribute was found.</span></span>

<span data-ttu-id="e4a92-110">Questo codice usa un gestore errori denominato **MyHandleError**.</span><span class="sxs-lookup"><span data-stu-id="e4a92-110">This code uses an error handler called **MyHandleError**.</span></span> <span data-ttu-id="e4a92-111">Per visualizzare l'implementazione di questo gestore errori, vedere l'argomento [**MyHandleError**](myhandleerror.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a92-111">To view the implementation for this error handler, see the [**MyHandleError**](myhandleerror.md) topic.</span></span>


```C++
#include <windows.h>

PCCERT_CONTEXT GetSignerCert(
        HCERTSTORE hCertStore)
//--------------------------------------------------------------------
//   Parameter passed in:
//      hCertStore, the handle of the store to be searched.
{
//--------------------------------------------------------------------
//   Declare and initialize local variables.

PCCERT_CONTEXT       pCertContext = NULL;
BOOL                 fMore = TRUE;
DWORD                dwSize = NULL;
CRYPT_KEY_PROV_INFO* pKeyInfo = NULL;
DWORD                PropId = CERT_KEY_PROV_INFO_PROP_ID;

//--------------------------------------------------------------------
//  Find certificates in the store until the end of the store
//  is reached or a certificate with an AT_SIGNATURE key is found.

while(fMore && 
  (pCertContext= CertFindCertificateInStore(
     hCertStore,           // Handle of the store to be searched.
     0,                    // Encoding type. Not used for this search.
     0,                    // dwFindFlags. Special find criteria.
                           // Not used in this search.
     CERT_FIND_PROPERTY,   // Find type that determines the kind of 
                           // search to do. In this case, search for 
                           // certificates that have a specific 
                           // extended property.
     &PropId,              // pvFindPara. Gives the specific 
                           // value searched for, here the identifier 
                           // of an extended property.
     pCertContext)))       // pCertContext is NULL for the 
                           // first call to the function. 
                           // If the function is called
                           // in a loop, after the first call
                           // pCertContext is the certificate
                           // returned by the previous call.
{
//-------------------------------------------------------------
// For simplicity, this code only searches 
// for the first occurrence of an AT_SIGNATURE key. 
// In many situations, a search would also look for a 
// specific subject name as well as the key type.

//-------------------------------------------------------------
// Call CertGetCertificateContextProperty once to get the
// returned structure size.

   if(!(CertGetCertificateContextProperty(
                 pCertContext,
                 CERT_KEY_PROV_INFO_PROP_ID,
                 NULL,
                 &dwSize)))
   {
      MyHandleError("Error Getting Key Property");
   }

//--------------------------------------------------------------
// Allocate memory for the returned structure.
    
   if(pKeyInfo)
        free(pKeyInfo);
   if(!(pKeyInfo = (CRYPT_KEY_PROV_INFO*)malloc(dwSize)))
   {
       MyHandleError("Error Allocating Memory for pKeyInfo");
   }
 
   //--------------------------------------------------------------
   // Get the key information structure.

   if(!(CertGetCertificateContextProperty(
       pCertContext,
       CERT_KEY_PROV_INFO_PROP_ID,
       pKeyInfo,
       &dwSize)))
   {
       MyHandleError("The second call to the function failed.");
   }
   
   //-------------------------------------------     
   // Check the dwKeySpec member for a signature key.
   if(pKeyInfo->dwKeySpec == AT_SIGNATURE)
   {
        fMore  = FALSE;
    }
}  // End of while loop

if(pKeyInfo)
   free(pKeyInfo);
return (pCertContext);
}  // End of GetSignerCert
```



 

 

---
description: Nell'esempio seguente vengono illustrati i passaggi per ottenere una \_ struttura del contesto del certificato che contiene un certificato. è necessario selezionare un certificato e un archivio certificati appropriati per l'applicazione.
ms.assetid: 31d7a8bd-729f-4db7-8e22-25d14296c0c4
title: Recupero di un certificato per Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf7f311ac31fe2ff033d4b57f7d04bd1f42424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310474"
---
# <a name="getting-a-certificate-for-schannel"></a><span data-ttu-id="07f31-103">Recupero di un certificato per Schannel</span><span class="sxs-lookup"><span data-stu-id="07f31-103">Getting a Certificate for Schannel</span></span>

<span data-ttu-id="07f31-104">Nell'esempio seguente vengono illustrati i passaggi per ottenere una struttura del [**\_ contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato che contiene un certificato. è necessario selezionare un certificato e un archivio certificati appropriati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="07f31-104">The following example shows the steps to obtain a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure that contains a certificate; you should select a certificate and certificate store that are appropriate for your application.</span></span>

<span data-ttu-id="07f31-105">In questo esempio viene illustrata l'apertura di un [*archivio certificati*](/windows/desktop/SecGloss/c-gly) e l'individuazione di un certificato che verrà passato alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , tramite la struttura di [**\_ cred di Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) .</span><span class="sxs-lookup"><span data-stu-id="07f31-105">This example demonstrates opening a [*certificate store*](/windows/desktop/SecGloss/c-gly) and locating a certificate that will be passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, by means of the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "crypt32.lib")

#define MACHINE_NAME "example server"

PCCERT_CONTEXT getServerCertificate ()
{
  HCERTSTORE hMyCertStore = NULL;
  PCCERT_CONTEXT aCertContext = NULL;
  
  //-------------------------------------------------------
  // Open the My store, also called the personal store.
  // This call to CertOpenStore opens the Local_Machine My 
  // store as opposed to the Current_User's My store.

    hMyCertStore = CertOpenStore(CERT_STORE_PROV_SYSTEM,
                                 X509_ASN_ENCODING,
                                 0,
                                 CERT_SYSTEM_STORE_LOCAL_MACHINE,
                                 L"MY");

  if (hMyCertStore == NULL) 
  {
    printf("Error opening MY store for server.\n");
    goto cleanup;
  }
  //-------------------------------------------------------
  // Search for a certificate with some specified
  // string in it. This example attempts to find
  // a certificate with the string "example server" in
  // its subject string. Substitute an appropriate string
  // to find a certificate for a specific user.

  aCertContext = CertFindCertificateInStore(hMyCertStore, 
                  X509_ASN_ENCODING, 
                  0,
                  CERT_FIND_SUBJECT_STR_A,
                  MACHINE_NAME, // use appropriate subject name
                  NULL
  );
  
  if (aCertContext == NULL)
  {
    printf("Error retrieving server certificate.");
    goto cleanup;
  }
cleanup:
  if(hMyCertStore)
  {
      CertCloseStore(hMyCertStore,0);
  }
  return aCertContext;
}
```



 

 

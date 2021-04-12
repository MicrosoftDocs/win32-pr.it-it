---
description: Nell'esempio seguente viene illustrato come un client tipico otterrebbe le credenziali Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Recupero delle credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345916"
---
# <a name="getting-schannel-credentials"></a>Recupero delle credenziali Schannel

Nell'esempio seguente viene illustrato come un client tipico otterrebbe le credenziali Schannel. L'esempio segue la procedura consigliata di utilizzo delle impostazioni predefinite del sistema per le crittografie e i punti di forza di crittografia. In questo modo, il pacchetto SChannel può utilizzare gli algoritmi più affidabili per proteggere il canale.


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



La differenza principale tra la richiesta lato client e lato server per le credenziali è che il server deve fornire un certificato usando una struttura [**del \_ contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato come indicato di seguito:


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



La funzione di esempio *getServerCertificate* è una funzione segnaposto per questa attività specifica dell'applicazione. Per un'implementazione di esempio della funzione *getServerCertificate* , vedere [recupero di un certificato](getting-a-certificate-for-schannel.md).

> [!Note]  
> Quando si richiedono le credenziali per l'uso da parte del server, modificare il terzo parametro (*fCredentialUse*) della funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) da SECPKG \_ cred in uscita \_ a SECPKG \_ cred in \_ ingresso.

 

 

 

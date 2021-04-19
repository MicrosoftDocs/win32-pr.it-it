---
description: Il supporto per la registrazione delle nuove funzionalità in un registro di sistema deve essere fornito nella nuova DLL insieme alla nuova funzione.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Registrazione della nuova funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317701"
---
# <a name="registering-the-new-functionality"></a>Registrazione della nuova funzionalità

Il supporto per la registrazione delle nuove funzionalità in un registro di sistema deve essere fornito nella nuova DLL insieme alla nuova funzione. Le [funzioni di supporto OID](cryptography-functions.md) forniscono assistenza per questa registrazione. Regsvr32.exe registra le nuove funzioni. Questo strumento è incluso in Windows.

La nuova DLL deve fornire punti di ingresso [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) per l'uso da parte di Regsvr32.exe. Le funzioni [*CryptoAPI*](../secgloss/c-gly.md) , ad esempio [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) o [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), possono essere usate all'interno di questi punti di ingresso, come illustrato nell'esempio seguente.


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



Questo esempio deve essere compilato e collegato alla nuova DLL. Questi due punti di ingresso, insieme al punto di ingresso della funzione, devono essere esportati.

Per installare la nuova funzionalità in un computer, eseguire Regsvr32.exe da un prompt dei comandi, specificando il nome e il percorso della nuova DLL. Regsvr32.exe accede alla funzione [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) tramite il punto di ingresso della funzione [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) e registra la nuova funzione e la nuova dll.

 

 

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
# <a name="registering-the-new-functionality"></a><span data-ttu-id="32ef9-103">Registrazione della nuova funzionalità</span><span class="sxs-lookup"><span data-stu-id="32ef9-103">Registering the New Functionality</span></span>

<span data-ttu-id="32ef9-104">Il supporto per la registrazione delle nuove funzionalità in un registro di sistema deve essere fornito nella nuova DLL insieme alla nuova funzione.</span><span class="sxs-lookup"><span data-stu-id="32ef9-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="32ef9-105">Le [funzioni di supporto OID](cryptography-functions.md) forniscono assistenza per questa registrazione.</span><span class="sxs-lookup"><span data-stu-id="32ef9-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="32ef9-106">Regsvr32.exe registra le nuove funzioni.</span><span class="sxs-lookup"><span data-stu-id="32ef9-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="32ef9-107">Questo strumento è incluso in Windows.</span><span class="sxs-lookup"><span data-stu-id="32ef9-107">This tool is included with Windows.</span></span>

<span data-ttu-id="32ef9-108">La nuova DLL deve fornire punti di ingresso [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) per l'uso da parte di Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="32ef9-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="32ef9-109">Le funzioni [*CryptoAPI*](../secgloss/c-gly.md) , ad esempio [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) o [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), possono essere usate all'interno di questi punti di ingresso, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="32ef9-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


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



<span data-ttu-id="32ef9-110">Questo esempio deve essere compilato e collegato alla nuova DLL.</span><span class="sxs-lookup"><span data-stu-id="32ef9-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="32ef9-111">Questi due punti di ingresso, insieme al punto di ingresso della funzione, devono essere esportati.</span><span class="sxs-lookup"><span data-stu-id="32ef9-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="32ef9-112">Per installare la nuova funzionalità in un computer, eseguire Regsvr32.exe da un prompt dei comandi, specificando il nome e il percorso della nuova DLL.</span><span class="sxs-lookup"><span data-stu-id="32ef9-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="32ef9-113">Regsvr32.exe accede alla funzione [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) tramite il punto di ingresso della funzione [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) e registra la nuova funzione e la nuova dll.</span><span class="sxs-lookup"><span data-stu-id="32ef9-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 

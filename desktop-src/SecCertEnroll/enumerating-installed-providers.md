---
description: Nell'esempio seguente viene illustrato come utilizzare l'API di registrazione del certificato per enumerare i provider installati in un computer.
ms.assetid: d7fa03d5-775c-41f3-9fef-8929bd25ed92
title: Enumerazione dei provider installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cddefe6cb85bc57c42313693ac86f4e2ea763d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882638"
---
# <a name="enumerating-installed-providers"></a><span data-ttu-id="1bfb7-103">Enumerazione dei provider installati</span><span class="sxs-lookup"><span data-stu-id="1bfb7-103">Enumerating Installed Providers</span></span>

<span data-ttu-id="1bfb7-104">Nell'esempio seguente viene illustrato come utilizzare l'API di registrazione del certificato per enumerare i provider installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-104">The following example shows how to use the Certificate Enrollment API to enumerate the providers installed on a computer.</span></span>

``` syntax
// enumeratinginstalledproviders.cpp : Defines the entry point for the console application.
//


/////////////////////////////////////////////////////////////////////
// EnumProviders.cpp 
//    Enumerate the cryptographic providers installed on the
//    computer. This sample enumerates the Cryptography API
//    (CryptoAPI) and Cryptography API: Next Generation (CNG) 
//    providers.

#include <certenroll.h>
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#include <atlbase.h>

// Forward declaration.
HRESULT enumProviders(void);

int _tmain(int argc, _TCHAR* argv[])
{
   UNREFERENCED_PARAMETER(argc);
   UNREFERENCED_PARAMETER(argv);

   HRESULT hr = S_OK;

   // Initialize COM.
   hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
   if(FAILED(hr)) return hr;

   // Enumerate the CryptoAPI and CNG providers.
   hr = enumProviders();

   CoUninitialize();
   return hr;
}

HRESULT enumProviders(void)
{
   CComPtr<ICspInformations>     pCSPs;   // Provider collection
   CComPtr<ICspInformation>      pCSP;    // Provider instgance
   HRESULT           hr          = S_OK;  // Return value
   long              lCount      = 0;     // Count of providers
   CComBSTR          bstrName;            // Provider name
   VARIANT_BOOL      bLegacy;             // CryptoAPI or CNG

   // Create a collection of cryptographic providers.
   hr = CoCreateInstance(
            __uuidof(CCspInformations),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(ICspInformations),
            (void **) &pCSPs);
   if(FAILED(hr)) return hr;

   // Add the providers installed on the computer.
   hr = pCSPs->AddAvailableCsps();
   if(FAILED(hr)) return hr;

   // Retrieve the number of installed providers.
   hr = pCSPs->get_Count(&lCount);
   if(FAILED(hr)) return hr;

   // Print the providers to the console. Print the
   // name and a value that specifies whether the 
   // CSP is a legacy or CNG provider.
   for (long i=0; i<lCount; i++)
   {
      hr = pCSPs->get_ItemByIndex(i, &pCSP);
      if(FAILED(hr)) return hr;

      hr = pCSP->get_Name(&bstrName);
      if(FAILED(hr)) return hr;

      hr = pCSP->get_LegacyCsp(&bLegacy);
      if(FAILED(hr)) return hr;

      if(VARIANT_TRUE == bLegacy)
         wprintf_s(L"%2d. Legacy: ", i);
      else
         wprintf_s(L"%2d. CNG: ", i);

      wprintf_s(L"%s\n", static_cast<wchar_t*>(bstrName.m_str));

      pCSP=NULL;

   }

   printf_s("\n\nHit any key to continue: ");
   _getch();

   return hr;

}
```

## <a name="related-topics"></a><span data-ttu-id="1bfb7-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bfb7-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bfb7-106">Informazioni sui provider di crittografia</span><span class="sxs-lookup"><span data-stu-id="1bfb7-106">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 




---
description: L'esempio seguente illustra come usare l'API di registrazione certificati per enumerare i provider installati in un computer.
ms.assetid: d7fa03d5-775c-41f3-9fef-8929bd25ed92
title: Enumerazione dei provider installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc29e017e78ecda9c8f3bf12ac0b9925c1817dee3de836b5cf6091bbe6ec3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779891"
---
# <a name="enumerating-installed-providers"></a>Enumerazione dei provider installati

L'esempio seguente illustra come usare l'API di registrazione certificati per enumerare i provider installati in un computer.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui provider del servizio di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

 




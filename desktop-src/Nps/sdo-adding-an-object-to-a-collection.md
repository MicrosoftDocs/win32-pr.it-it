---
title: Aggiunta di un oggetto a una raccolta
description: Aggiunta di un oggetto a una raccolta
ms.assetid: fc62698d-0bb9-478c-91cf-9f8fec36dba4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1990829e88d54838dbce2658c914ceff602d8e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300148"
---
# <a name="adding-an-object-to-a-collection"></a>Aggiunta di un oggetto a una raccolta

Il codice seguente aggiunge un nuovo criterio alla raccolta di criteri IAS. La variabile pClientsCollection punta a un'interfaccia [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) per la raccolta. Per informazioni su come recuperare l'oggetto raccolta, vedere [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection) .


```C++
   HRESULT hr;
   _bstr_t      bstrClientName = L"Test Client";
   VARIANT_BOOL vbNameUnique = VARIANT_FALSE;

   //
   // Check if the new client's name is unique
   //

   hr = pClientsCollection->IsNameUnique(bstrClientName, &vbNameUnique);
   if (FAILED(hr))
   {
      return hr;
   }

   if (VARIANT_FALSE == vbNameUnique)
   {
      //
      // The name is not unique. Handle the error
      //
      return E_FAIL;
   }

   //
   // Name is unique. Add the client.
   //
   CComPtr<IDispatch> pClientDispatch;
   pClientDispatch.p = NULL;
   hr = pClientsCollection->Add(bstrClientName, &pClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pClientSDO;
   hr = pClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void**) &pClientSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Set the address for the client
   //
   _variant_t  vtClientAddress = L"127.0.0.1";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_ADDRESS, &vtClientAddress);
   if (FAILED(hr))
   {
      return hr;
   }
       
   //
   // Set the shared secret for the client
   //
   _variant_t  vtClientSecret = L">@U#'6cc='5Ly9O5QKEj2RTJr*fM";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_SHARED_SECRET, &vtClientSecret);
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Apply the changes
   //
   hr = pClientSDO->Apply();
   if (FAILED(hr))
   {
      return hr;
   }   
    
   //
   // Refresh the service using a ISdoServiceControl interface retrieved
   // in the code sample "Retrieve a Service SDO"
   //
   hr = pSdoServiceControl->ResetService();
   if (FAILED(hr))
   {
      //
      // If IAS is not installed or is not running then ignore the error
      //  
   }


```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_BSTR \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278286(v=vs.60))
</dt> <dt>

[**ISdoCollection:: Add**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add)
</dt> <dt>

[**ISdoCollection::IsNameUnique**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique)
</dt> <dt>

[Recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**VARIANTE**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 
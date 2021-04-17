---
title: Recupero di un oggetto da una raccolta
description: Recupero di un oggetto da una raccolta
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8d5bfcba8a1671c7824a4b1356e9c8e1dd7567
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516935"
---
# <a name="retrieving-an-object-from-a-collection"></a><span data-ttu-id="0baef-103">Recupero di un oggetto da una raccolta</span><span class="sxs-lookup"><span data-stu-id="0baef-103">Retrieving an Object from a Collection</span></span>

<span data-ttu-id="0baef-104">Il codice seguente recupera l'indirizzo IP di un client da una raccolta di client.</span><span class="sxs-lookup"><span data-stu-id="0baef-104">The following code retrieves the IP address of a client from a collection of clients.</span></span> <span data-ttu-id="0baef-105">La variabile pClientsCollection punta a un'interfaccia [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="0baef-105">The variable pClientsCollection points to an [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface for the collection.</span></span> <span data-ttu-id="0baef-106">Per informazioni su come recuperare l'oggetto raccolta, vedere [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection) .</span><span class="sxs-lookup"><span data-stu-id="0baef-106">See [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) for information on how to retrieve the collection object.</span></span>


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="0baef-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0baef-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0baef-108">**ISdoCollection:: Item**</span><span class="sxs-lookup"><span data-stu-id="0baef-108">**ISdoCollection::Item**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[<span data-ttu-id="0baef-109">Recupero di una raccolta</span><span class="sxs-lookup"><span data-stu-id="0baef-109">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="0baef-110">**SysAllocString**</span><span class="sxs-lookup"><span data-stu-id="0baef-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="0baef-111">**SysFreeString**</span><span class="sxs-lookup"><span data-stu-id="0baef-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[<span data-ttu-id="0baef-112">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="0baef-112">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 
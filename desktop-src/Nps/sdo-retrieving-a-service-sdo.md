---
title: Recupero di un servizio SDO
description: Recupero di un servizio SDO
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223960"
---
# <a name="retrieving-a-service-sdo"></a><span data-ttu-id="0a2dc-103">Recupero di un servizio SDO</span><span class="sxs-lookup"><span data-stu-id="0a2dc-103">Retrieving a Service SDO</span></span>

> [!Note]  
> <span data-ttu-id="0a2dc-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0a2dc-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="0a2dc-105">Il codice seguente recupera un oggetto dati server (SDO) per il server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="0a2dc-105">The following code retrieves a Server Data Object (SDO) for the Network Policy Server .</span></span>


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a><span data-ttu-id="0a2dc-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a2dc-106">Remarks</span></span>

<span data-ttu-id="0a2dc-107">Prima di poter chiamare uno dei metodi [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) , è necessario [connettersi](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) a un computer.</span><span class="sxs-lookup"><span data-stu-id="0a2dc-107">You must [attach](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) to a computer before you can call any of the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a2dc-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a2dc-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a2dc-109">Connessione a un computer SDO-Enabled</span><span class="sxs-lookup"><span data-stu-id="0a2dc-109">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="0a2dc-110">**ISdoMachine::GetServiceSDO**</span><span class="sxs-lookup"><span data-stu-id="0a2dc-110">**ISdoMachine::GetServiceSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[<span data-ttu-id="0a2dc-111">**ISdoServiceControl**</span><span class="sxs-lookup"><span data-stu-id="0a2dc-111">**ISdoServiceControl**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 
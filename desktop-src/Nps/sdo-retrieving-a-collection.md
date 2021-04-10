---
title: Recupero di una raccolta
description: Recupero di una raccolta
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963263"
---
# <a name="retrieving-a-collection"></a><span data-ttu-id="c187b-103">Recupero di una raccolta</span><span class="sxs-lookup"><span data-stu-id="c187b-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="c187b-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c187b-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c187b-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="c187b-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c187b-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="c187b-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c187b-107">Il codice seguente recupera la raccolta client per il server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="c187b-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a><span data-ttu-id="c187b-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c187b-108">Remarks</span></span>

<span data-ttu-id="c187b-109">La variabile pSdoServiceControl contiene un puntatore a un oggetto dati server per NPS.</span><span class="sxs-lookup"><span data-stu-id="c187b-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="c187b-110">Per ulteriori informazioni, vedere l'argomento [recupero di un servizio SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="c187b-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="c187b-111">La variabile vtClientsCollection è di tipo [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="c187b-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="c187b-112">Un \_ \_ oggetto Variant t incapsula o racchiude il tipo di dati [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="c187b-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="c187b-113">La classe gestisce l'allocazione e la deallocazione delle risorse e effettua chiamate di funzione a [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c187b-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="c187b-114">Dopo la chiamata a "pSdo->GetProperty ()", la variabile vtProtocolsCollection specifica un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c187b-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="c187b-115">Il membro **pdispVal** di vtProtocolsCollection contiene un puntatore all'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c187b-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="c187b-116">Il codice di esempio precedente può essere adattato per recuperare altre raccolte NPS, ad esempio le raccolte di gestori di richieste NPS.</span><span class="sxs-lookup"><span data-stu-id="c187b-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="c187b-117">I valori enumerati del tipo di enumerazione [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) che corrispondono alle raccolte NPS disponibili.</span><span class="sxs-lookup"><span data-stu-id="c187b-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c187b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c187b-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c187b-119">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="c187b-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="c187b-120">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="c187b-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="c187b-121">**ISdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="c187b-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="c187b-122">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="c187b-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="c187b-123">Recupero di un servizio SDO</span><span class="sxs-lookup"><span data-stu-id="c187b-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="c187b-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="c187b-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="c187b-125">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="c187b-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="c187b-126">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="c187b-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 
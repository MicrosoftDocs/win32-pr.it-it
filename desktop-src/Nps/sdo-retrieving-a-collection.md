---
title: Recupero di una raccolta
description: Recupero di una raccolta
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343f00ee28475d1e6180646a0e548c18d51701afed587c99582dad7dc60d094c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063311"
---
# <a name="retrieving-a-collection"></a>Recupero di una raccolta

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

Il codice seguente recupera la raccolta di client per il server dei criteri di rete.


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



## <a name="remarks"></a>Commenti

La variabile pSdoServiceControl contiene un puntatore a un oggetto dati del server per Server dei criteri di rete. Per altre informazioni, vedere l'argomento [Recupero di un SDO del servizio.](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)

La variabile vtClientsCollection è di tipo [ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un \_ oggetto variant t incapsula o racchiude il tipo di dati \_ [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) La classe gestisce l'allocazione e la deallocazione delle risorse e effettua chiamate di funzione [**a VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) in base alle esigenze.

Dopo la chiamata a "pSdo->GetProperty()", la variabile vtProtocolsCollection specifica un oggetto. Il **membro pdispVal** di vtProtocolsCollection contiene un puntatore [**all'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) per l'oggetto.

Il codice di esempio precedente può essere adattato per recuperare altre raccolte di Server dei criteri di rete, ad esempio le raccolte gestori richieste NPS. I valori enumerati del tipo di enumerazione [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) che corrispondono alle raccolte di Server dei criteri di rete disponibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**PROPRIETÀ IAS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Recupero di un SDO del servizio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 
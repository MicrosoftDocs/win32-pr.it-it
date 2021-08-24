---
title: Enumerazione di oggetti in una raccolta
description: Enumerazione di oggetti in una raccolta
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0399a75e9301fcdb5e88e6f30b7e0b2ef66160fa05136ed43b51fa8e80eca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742111"
---
# <a name="enumerating-objects-in-a-collection"></a>Enumerazione di oggetti in una raccolta

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

Il codice seguente enumera i protocolli nella raccolta di protocolli NPS.


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a>Commenti

Le variabili vtName e vtProtocol sono di tipo [ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un [ \_ oggetto variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) incapsula o racchiude il tipo di dati **VARIANT.** La classe gestisce l'allocazione e la deallocazione delle risorse e effettua chiamate di funzione [**a VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[Aggiunta di un client](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[Recupero di un SDO del servizio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 
---
title: Accesso agli attributi con l'interfaccia IDirectoryObject
description: L'interfaccia IDirectoryObject fornisce un'applicazione client scritta in C e C++ con accesso diretto agli oggetti del servizio directory.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Accesso agli attributi con l'interfaccia IDirectoryObject ADSI
- IDirectoryObject ADSI, accesso agli attributi con
- ADSI ADSI, utilizzo di, utilizzo dell'interfaccia IDirectoryObject per l'accesso agli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955123"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Accesso agli attributi con l'interfaccia IDirectoryObject

L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornisce un'applicazione client scritta in C e C++ con accesso diretto agli oggetti del servizio directory. L'interfaccia consente l'accesso per mezzo di un protocollo di rete diretto, anziché tramite la cache degli attributi ADSI. Al posto delle proprietà supportate dall'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** fornisce metodi che supportano un subset critico dei metodi di manutenzione di un oggetto e forniscono l'accesso ai relativi attributi. Con **IDirectoryObject**, un client può ottenere o impostare un numero qualsiasi di attributi di oggetto con una chiamata al metodo. A differenza dei metodi di automazione corrispondenti, che vengono in batch, quelli di **IDirectoryObject** vengono eseguiti quando vengono chiamati. Poiché i metodi su questa interfaccia non richiedono la creazione di un'istanza di un oggetto directory di automazione, il sovraccarico delle prestazioni è ridotto.

I client scritti in linguaggi come C e C++ devono usare i metodi dell'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per ottimizzare le prestazioni e sfruttare le interfacce del servizio directory native. I client di automazione non possono usare **IDirectoryObject**. Ma devono usare l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .

Il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera gli attributi con valori singoli e multipli. Questo metodo accetta un elenco di attributi richiesti e restituisce una [**struttura \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) . ADSI alloca questa struttura; il chiamante deve liberare questa memoria quando non è più necessaria mediante la funzione [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

L'ordine dei valori di attributo restituiti non corrisponde necessariamente all'ordine in cui gli attributi sono stati richiesti. È pertanto necessario confrontare i nomi di attributo restituiti da ADSI.

> [!Note]  
> La struttura di [**\_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) non restituisce tutti gli attributi richiesti. Solo gli attributi che contengono valori fanno parte della struttura restituita.

 

Il numero di attributi restituiti è determinato dal parametro *dwNumberAttributes* passato al metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .

Nell'esempio di codice seguente viene associato a un oggetto e viene utilizzato il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) per recuperare gli attributi dell'oggetto.


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




